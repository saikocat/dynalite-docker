# Introduction
Small docker container (Alpine based) with service user (`app`) and mountable volume (`/data/dynalite`) using __[Kinesalite](https://github.com/mhart/dynalite)__ - by [@mhart](http://www.github.com/mhart/dynalite)

# Build Instruction
```
$ docker build -t saikocat/dynalite:1.0.3 .
```

# Run Instruction
```
$ docker pull saikocat/dynalite
# 5678 is the host port, --port 4567 must be present since it is the exposed port
$ docker run -d \
    -p 5678:4567 \
    --name dynalite \
    saikocat/dynalite:1.0.3 --port 4567
```

## Runtime Configuration
More runtime flags can be found at __[Dynalite](https://github.com/mhart/dynalite)__

## Persistent volume
`-v host/dynalite:/data/dynalite` and `--path /data/dynalite`
if you want persistency
