# fping-docker
A containerised version of [fping](https://fping.org/).

## Building the container
```bash
docker build -t fping-docker:latest
```
## Running the container
```bash
docker run --rm fping-docker <FPING_ARGS>

## Example:
docker run --rm fping-docker -A -d -a -q -g -a -i 1 -r 0 192.168.1.0/24
```

## Dockerfile Entrypoint
```dockerfile
ENTRYPOINT ["/sbin/tini", "--", "/usr/sbin/fping"]
```
