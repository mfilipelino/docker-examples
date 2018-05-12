# Build Parameters



## CASE 1

### build

```bash
docker image build -t build-parameters .
``` 

### run 

```bash
docker container run parameters bash -c 'echo $VAR_PRINT'
```

### out

```bash
Hello
```

## CASE 2

### build

```bash
docker image build -t build-parameters --build-arg VAR_PRINT=CASE2 .
``` 

### run 

```bash
docker container run parameters bash -c 'echo $VAR_PRINT'
```


### out

```bash
CASE2
```
