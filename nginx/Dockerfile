FROM nginx
MAINTAINER James Hanlon

RUN mkdir /etc/nginx/sites-available && \
    mkdir /etc/nginx/sites-enabled

COPY nginx.conf /etc/nginx/nginx.conf
COPY website.conf /etc/nginx/sites-available
COPY uwsgi_params /tmp

RUN rm /etc/nginx/conf.d/default.conf && \
    ln -s /etc/nginx/sites-available/website.conf \
          /etc/nginx/sites-enabled/website.conf
