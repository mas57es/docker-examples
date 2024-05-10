
### Step 3: Build Docker Image
Open a terminal, navigate to the project directory, and run the following command to build the Docker image:

```bash
docker build -t jupyter .
```

Step 4: Run Docker Container
Once the image is built, execute the following command to run a Docker container:

```
docker run -p 8888:8888 jupyter
```