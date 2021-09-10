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

# 参考

- [PythonでUnixドメインソケットを使って通信する \- 偏った言語信者の垂れ流し](https://tokibito.hatenablog.com/entry/20150927/1443286053)
