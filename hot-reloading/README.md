##2. Hot Reloading with Nodemon
```bash
docker build -t node-hot-reload-docker .
docker run --rm -it -p 8080:8080 -v $(pwd):/app  node-hot-reload-docker bash
```