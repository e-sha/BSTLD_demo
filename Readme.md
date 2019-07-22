# BSTLD-demo

A sample project to train and evaluate model on BSTLD.

# Install

1. Download and extract BSTLD dataset to `<data_dir>`
1. Download and extract pretrained models to `<trained_dir>`
1. Build a container
```bash
docker build -f Dockerfile.gpu . -t bstld.latest
```

# Run a container
1. Exec
```bash
nvidia-docker run -p 8889:8888 -v <data_dir>:/root/data -v <trained_dir>:/root/trained bstld:latest
```
1. Open the URL: localhost:8889
