## Running with Docker

To run this project using **Docker**, follow these steps:

1. Make sure you have [Docker](https://docs.docker.com/get-docker/) installed on your system.

2. Clone this repository:
   git clone https://github.com/your-username/your-repo.git
   cd your-repo
   
3. Build the Docker image:
   docker build -t project-name .

4. Run the container:
   docker run -it --rm -p 8080:8080 project-name

   -it: starts an interactive terminal.

   --rm: removes the container once it stops.

   -p 8080:8080: maps port 8080 from the container to your local machine. Change it if your app uses a different port.

5. Open your browser and go  to:
   http://localhost:8080

Using Docker Compose (optional)

If you prefer using Docker Compose, you can create a docker-compose.yml file like this:

version: "3"
services:
  app:
    build: .
    ports:
      - "8080:8080"

Then run:

docker-compose up --build



