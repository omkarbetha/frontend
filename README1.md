# frontend

The frontend is the service in TODO to serve the web content over Nginx.

To install Nginx

apt update
apt install nginx
systemctl enable nginx
systemctl start nginx

cd /var/www/html

Now create a directory vue

mkdir vue
cd vue

Clone the repo into the vue directory

git clone https://github.com/zelar-soft-todoapp/frontend.git

Now change the path of Nginx to frontend

vim /etc/nginx/sites-available/default

Change the path to root 

/var/www/html/vue/frontend/dist;

Now restart the services

systemctl restart nginx
systemctl enable nginx
