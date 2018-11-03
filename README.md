# React demo

## Docker

remove node_modules before build, a little faster

### build dev

```bash
docker build -f Dockerfile.dev .
```

### run dev

```bash
# ignore node_modules only mount everything else in the project folder $(pwd) to /app in the container
$ docker run -p 3000:3000 -v /app/node_modules -v $(pwd):/app <image_id>

# or
$ docker-compose up
# goto http://localhost:3000/
```

### test

```bash
docker run -it <image_id> npm run test
# or
$ docker-compose up
```

### build prod

```bash
docker build .
```

### run prod

```bash
$ docker run -p 8080:80 <image_id>
# goto http://localhost:8080/
```

## aws

* create an aws `elasticbeanstalk` instance
* update deploy config in the `travis.yml`, if needed
* `git push origin master`

## see also

[udemy docker and kubernetes](https://www.udemy.com/docker-and-kubernetes-the-complete-guide/learn/v4/content)