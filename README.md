# React demo

## Docker

remove node_modules before build

### build dev

```bash
docker build -f Dockerfile.dev .
```

### run dev

```bash
# ignore node_modules only mount everything else in the project folder $(pwd) to /app in the container
docker run -p 3000:3000 -v /app/node_modules -v $(pwd):/app <image_id>

# or
docker-compose up
```

### test dev

```bash
docker run -it <image_id> npm run test
```

## see also

[udemy docker and kubernetes](https://www.udemy.com/docker-and-kubernetes-the-complete-guide/learn/v4/content)