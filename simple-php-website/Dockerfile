FROM ubuntu:18.04
WORKDIR /var/www/html


ENV TZ=Asia/kolkata
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN apt update -y && apt install software-properties-common -y  && apt install -y  tzdata

RUN add-apt-repository ppa:ondrej/php && apt update -y
RUN apt install -y php7.3 php7.3-cli php7.3-fpm php7.3-json php7.3-pdo php7.3-mysql php7.3-zip php7.3-gd  php7.3-mbstring php7.3-curl php7.3-xml php7.3-bcmath php7.3-json nginx net-tools libapache2-mod-php7.3  php7.3-intl vim curl

COPY default.conf /etc/nginx/conf.d/default.conf


