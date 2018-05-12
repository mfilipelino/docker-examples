# First-build

## build

```bash
docker image build -t first-image .
```

## run

```bash
docker container run -p 80:80 first-image
```

## test

```bash
curl http://localhost:80
<h1> Hello World </h1>
```

