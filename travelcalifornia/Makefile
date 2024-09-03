.PHONY: docker-build docker-run
docker-build:
	@echo "Building the Docker image..."
	@docker build -t travelcalifornia .

docker-run:
	@echo "Running the Docker container..."
	@docker run --rm --name travelcalifornia -p 5001:80 travelcalifornia

docker-stop:
	@echo "Stopping the Docker container..."
	@docker stop travelcalifornia
