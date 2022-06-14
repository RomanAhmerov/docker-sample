run:
	docker run -d -p 3000:4200 -v logs:/app/data --rm --name logsapp logsapp:volumes
run-dev:
	docker run -d -p 3000:4200 -v "/Users/roman/Desktop/GitHub/docker-sample/logs-app:/app" -v /app/node_modules -v logs:/app/data --rm --name logsapp logsapp:volumes
stop: 
	docker stop logsapp