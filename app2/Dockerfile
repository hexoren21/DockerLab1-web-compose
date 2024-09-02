FROM ubuntu
RUN apt update
RUN apt install wget unzip apache2 unzip -y
RUN wget https://www.tooplate.com/zip-templates/2135_mini_finance.zip -P /tmp/
RUN unzip /tmp/2135_mini_finance.zip -d /tmp/
RUN mv /tmp/2135_mini_finance/* /var/www/html
RUN sed -i 's/Listen 80/Listen 8080/' /etc/apache2/ports.conf
RUN sed -i 's/:80/:8080/' /etc/apache2/sites-available/000-default.conf
CMD ["apachectl", "-D", "FOREGROUND"]  
