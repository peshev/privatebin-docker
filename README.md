```
git clone git@github.com:peshev/privatebin-docker.git
cd privatebin-docker
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout proxy/ssl/privatebin.key -out proxy/ssl/privatebin.crt -subj "/C=US/L=My-City/O=My-Organiszation/CN=my-hostname"
mkdir -p privatebin-data
docker-compose build
docker-compose up -d
```
