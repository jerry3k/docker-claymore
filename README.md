# DO NOT USE - gives error
`
▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒ͻ
▒      Claymore's Dual ETH + DCR/SC/LBC/PASC GPU Miner v9.5      ▒
▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒ͼ

ETH: 2 pools are specified
Main Ethereum pool is eth-eu1.nanopool.org:9999
SC: 2 pools are specified
Main Siacoin pool is sia-eu1.nanopool.org:7777
AMD OpenCL platform not found
No NVIDIA CUDA GPUs detected.
No AMD OPENCL or NVIDIA CUDA GPUs found, exit
`
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
  -e "DWAL=d2ce0ab59206119c0ba30b1592c8c43a6c3f949cd1eafc41cba7791d5f74d801a4e5bac8f463" \
  geoah/docker-claymore:v0.0.1
```
