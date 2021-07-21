## Deepstream Demos

### Prerequisites
Register NGC API Key at https://ngc.nvidia.com/

Log in nvcr.io
```
docker login nvcr.io
```

Pull DeepStream image
```
docker pull nvcr.io/nvidia/deepstream:5.1-21.02-triton
```

Clone repository
```
git clone https://github.com/spoonnvidia/ds-demo
```

Create DeepStream Container
```
sudo docker run --gpus all -it --network=host -v $(pwd)/ds-demo:/opt/nvidia/deepstream/deepstream-5.1/notebooks && \
   -v /tmp/.X11-unix:/tmp/.X11-unix -e DISPLAY=:0 -w /opt/nvidia/deepstream/deepstream-5.1 nvcr.io/nvidia/deepstream:5.1-21.02-triton
```

### Usage
Enter DeepStream container and run the demos
