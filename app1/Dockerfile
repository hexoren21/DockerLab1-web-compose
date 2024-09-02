FROM ubuntu 
RUN apt update
RUN apt install wget unzip nginx -y
RUN rm -rf /var/www/html/*
RUN wget https://www.tooplate.com/zip-templates/2137_barista_cafe.zip -P /tmp/
RUN unzip /tmp/2137_barista_cafe.zip -d /tmp/
RUN mv /tmp/2137_barista_cafe/* /var/www/html/
CMD ["nginx","-g", "daemon off;"]

