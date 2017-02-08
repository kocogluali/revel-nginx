revel-nginx
Revel Nginx

/etc/nginx/nginx.conf 


server {
        listen 80;

        root /usr/share/nginx/html; 
        index index.html index.htm;

        server_name site_adınız(a.com);

                location / {
                        proxy_pass      http://127.0.0.1:9000;
                }
        }

}


Revel app 'ımızın içerisindeki app.conf bu ayalarıda ekliyoruz..

####

http.addr="127.0.0.1"
http.port=9000

#####

Revel projemizi run edelim ve nginx yeniden başlatalım. 

UYARI : Eğer siteye erişelemiyorsa 9000 portunu güvenlik duvarında izin verin. 
FAYDALI : screen -mlS revel run app_name ile arka planda çalıştırmış olursunuz.
