# helm

test helm 
1.
mkdir app
cd  app
vi index.html

<h1>Hello World!!!</h1>

cd ..
vi Dockerfile

FROM busybox
ADD app/index.html /www/index.html
EXPOSE 8005
CMD httpd -p 8005 -h /www; tail -f /dev/null

docker build -t helloworld .
