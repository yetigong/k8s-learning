.PHONY: docker-build docker-run docker-stop
docker-build:
	@echo "Building the Docker image..."
	@docker build -t travelcalifornia .

docker-run:
	@echo "Running the Docker container..."
	@docker run --rm --name travelcalifornia -p 5001:80 travelcalifornia

docker-stop:
	@echo "Stopping the Docker container..."
	@docker stop travelcalifornia

create_docker_registry:
	@echo "Creating a Docker registry..."
	@container_id=$$(docker ps -a | grep 'registry' | awk '{ print $$1 }'); \
	echo "registry process is $$container_id"; \
	if docker ps -a | grep -q 'registry'; \
		then echo "Registry already exists"; \
	else docker run -d -p 50001:5000 --restart=always --name registry registry:2; \
	fi