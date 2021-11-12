FROM ubuntu:18.04
WORKDIR /var/www/html


ENV TZ=Asia/kolkata
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN apt update -y && apt install software-properties-common -y  && apt install -y  tzdata

RUN add-apt-repository ppa:ondrej/php && apt update -y
RUN apt install -y php7.3 php7.3-cli php7.3-fpm php7.3-json   nginx net-tools  vim curl netcat


COPY . .
COPY default.conf /etc/nginx/conf.d/default.conf
COPY nginx.conf  /etc/nginx/nginx.conf
RUN chown -R www-data /var/www/html


CMD service php7.3-fpm start && nginx -g 'daemon off;'


