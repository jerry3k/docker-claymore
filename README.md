# Claymore Eth Miner for NVIDIA GPUs

This is a very crude container based on nvidia's cuda containers
and the Claymore Eth dual miner.  
It is mainly meant to be used for dual mining eth/sia on nanopool.  
If you need to mine something different or somewhere else you might
need to modify some more env vars or even the entrypoint script.

## Running

You need to specify a number or required env vars.

* `EMAIL` Your email.
* `WORKER` Your worker name.
* `EWAL` Ethereum wallet address.
* `DWAL` Sia wallet address.

Check out the `Dockerfile` for the rest of the optional env vars supported.  
Claymore supports quite a few more that are not being used here.

### Example

```
docker run \
  -e "EMAIL=jerry3k@hotmail.com" \
  -e "WORKER=docker1" \
  -e "EWAL=0x50210a4a578d10346ead3a770e888ca749a4bccb" \
  geoah/docker-claymore:v0.0.1
```
