# dentalspeed
Teste Magento Dental Speed
Procedimento de Instalação
Ambiente Linux - VMWare

Instalação do LAMP - Comandos
sudo apt-get install apache2
Download  do .deb na página de download MySQL, porém utilizei a versão 5.7 e não 8
cd ~/Downloads
sudo dpkg -i mysql-apt-config*.deb

sudo apt-get update
sudo apt-get install mysql-server

Utilizei a versão 7.3 do PHP

sudo apt-get -y update
sudo add-apt-repository ppa:ondrej/php
sudo apt-get -y update
sudo apt-get install -y php7.3 libapache2-mod-php7.3 php7.3-common php7.3-gd php7.3-mysql php7.3-curl php7.3-intl php7.3-xsl php7.3-mbstring php7.3-zip php7.3-bcmath php7.3-iconv php7.3-soap

Setei em apache2.conf um grupo com o meu usuário

user renato
group renato

atribui permissão a pasta var/www ao meu usuário e permissão de leitura  e escrita da pasta

sudo chown -R renato:renato /var/www/
sudo chmod  -R 770 /var/www/

Ativei para o Magento o modo de reescrita do Apache
sudo  a2enmod  rewrite

Alterei dentro do apache2.conf
<Directory /var/www/> 
Options Indexes FollowSymLinks 
AllowOverride All

Fiz o download com SampleData da versão Magento 3.6 - Testei tando via composer quanto via download

Fiz a instalação Manual

O primeiro commit que fiz, não add todos os arquivos do Magento, devido ao tamanho do mesmo, o Github retornou erro devido ao tamanho ser superior à 100MB.
Fiz este com alguns arquivos para verificar que a instalação foi realizada.


MODULO
