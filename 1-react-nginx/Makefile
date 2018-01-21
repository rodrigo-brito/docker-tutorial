yarn:
	docker run --rm -w /app -v $(PWD):/app node:alpine yarn
build: yarn
	docker run --rm -w /app -v $(PWD):/app node:alpine sh -c "yarn build"
dev: yarn
	docker run -ti --rm -w /app -v $(PWD):/app -p 8080:3000 node:alpine sh -c "yarn start"
	echo "Development server available at http://localhost:8080"
test: yarn
	docker run -ti --rm -w /app -v $(PWD):/app -p 8080:3000 node:alpine sh -c "yarn test"
prod: build
	docker run -ti --rm --name my-nginx -p 8080:80 -v $(PWD)/build:/usr/share/nginx/html nginx