FROM nginx:latest
LABEL "PROJECT"="Vprofile-v2"
LABEL  "Author"="Kingdave"

#RUN rm -rf /etc/nginx/nginx.conf
RUN rm -rf /etc/nginx/conf.d/default.conf

#COPY nginvproapp.conf /etc/nginx/vproapp.conf

COPY nginvproapp.conf /etc/nginx/conf.d/nginvproapp.conf

#COPY nginvproapp.conf /etc/nginx/conf.d/vproapp.conf
