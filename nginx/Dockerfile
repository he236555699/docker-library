FROM nginx:latest

RUN{ \
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
	} > /etc/mysql/conf.d/docker.cnf

EXPOSE 80
CMD ["nginx"]