# Build
```shell
docker build --no-cache -t kindest/node:toolkit .
```

# Use
```shell
./nvkind cluster create --image=kindest/node:toolkit
```
# Note
__Must run using the `nvkind` compiled from the `local` branch__