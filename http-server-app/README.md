## http-server-python

### build

```bash
docker image build -t http-server-python .
```

### run

```bash
docker container run -it -p 80:8000 -v $(pwd):/app --name server-instance http-server-python
```

### test

```
curl localhost:80
```


### output

```bash
<h1> Hello from python </h1>
```


### cat loging

```bash
docker container run -it --volumes-from=server-instance debian cat /log/http-server.log
```