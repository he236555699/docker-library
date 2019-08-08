FROM nginx:latest

RUN { \
<<<<<<< HEAD
		echo ''; \
		echo 'stream {'; \
		echo '	server {'; \
		echo '		listen 80;'; \
		echo '		server_name */mysql;'; \
		echo '		proxy_connect_timeout 1s;'; \
		echo '		proxy_timeout 3s;'; \
		echo '		proxy_pass kube-dns.kube-system.svc.cluster.local:3306;'; \
		echo '	}'; \
		echo '}'; \
	} > /etc/nginx/nginx.conf

EXPOSE 80
CMD ["nginx"]
=======
		echo 'http {'; \
		echo '	stream {'; \
		echo '		server {'; \
		echo '			listen 80;'; \
		echo '			server_name */mysql;'; \
		echo '			proxy_connect_timeout 1s;'; \
		echo '			proxy_timeout 3s;'; \
		echo '			proxy_pass mysql-56-server.development;'; \
		echo '		}'; \
		echo '	}'; \
		echo '}'; \
	} > /etc/nginx/conf.d/server.conf

EXPOSE 80
CMD ["nginx"]
>>>>>>> a6edf372fa6957393b969cf060f2adee59c9a72e
