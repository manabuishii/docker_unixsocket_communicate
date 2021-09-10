# docker_unixsocket_communicate

From docker to host via unix socket sample

# how to execute

## Server (host) side

```
python3 server.py
```

## Client side (docker)

### As CLI


```
docker run --rm -w /work -v $PWD:/work -ti python:3.9.6 python3 /work/client.py
```

### In bash

```
docker run --rm -w /work -v $PWD:/work -ti python:3.9.6 python3 /bin/bash
```

and

```
python3 client.py
```


## Example output

```console
$ docker run --rm -w /work -v $PWD:/work -ti python:3.9.6 python3 /work/client.py
send to server (0): sbatch ./hello.sh
receive from server:
Submitted batch job 12

send to server (1): sbatch ./hello.sh
receive from server:
Submitted batch job 13

send to server (2): sbatch ./hello.sh
receive from server:
Submitted batch job 14
```

# 参考

- [PythonでUnixドメインソケットを使って通信する \- 偏った言語信者の垂れ流し](https://tokibito.hatenablog.com/entry/20150927/1443286053)
