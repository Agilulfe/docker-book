install:
	npm install

build:
	docker build -t example/docker-node-hello:latest .

run:
	node index.js

run-container:
	docker run -p 8080:8080 -d example/docker-node-hello:latest

check-status:
	docker ps

add-argument:
	docker run -p 8080:8080 -d -e WHO="Guillaume" example/docker-node-hello:latest

test:
	curl localhost

clean:
	rm -rf node_modules

change-tag:
	docker tag example/docker-node-hello:latest gujacobs/docker-node-hello:latest

check-image:
	docker image ls gujacobs/docker-node-hello

push:
	docker push gujacobs/docker-node-hello:latest


.PHONY: install build run test clean
