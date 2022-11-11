.PHONY:start
start:
	docker compose up -d

.PHONY:restart
restart:
	make rm
	docker compose pull
	make start

.PHONY:rm
rm:
	docker compose stop
	docker compose rm -f

.PHONY: cert
cert:
	docker compose run --rm  certbot certonly --webroot --webroot-path /var/www/certbot/ -d dreamrounder.com
	docker compose run --rm  certbot certonly --webroot --webroot-path /var/www/certbot/ -d blog.dreamrounder.com
	docker compose run --rm  certbot certonly --webroot --webroot-path /var/www/certbot/ -d resume.dreamrounder.com