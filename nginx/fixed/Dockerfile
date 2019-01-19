FROM richarvey/nginx-php-fpm

RUN wget -O /tmp/bwapp.zip https://sourceforge.net/projects/bwapp/files/latest/download && \
  unzip /tmp/bwapp.zip bWAPP/* && mv bWAPP/* . && rm -rf bwapp*

RUN sed -i 's/db_password = "bug"/db_password = ""/g' admin/settings.php
RUN sed -i 's/db_server = "localhost"/db_server = "mysql"/g' admin/settings.php