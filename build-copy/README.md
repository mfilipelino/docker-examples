# build copy

## build

```bash
docker image build -t build-copy .
```

## run
```
docker container run build-copy -p 80:80
```

## test

```bash
curl localhost:80
```

## out

```bash
<h1> COPY FILE <h1>
```
