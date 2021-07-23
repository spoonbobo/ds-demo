## Deepstream Demos

### Prerequisites

You can use pre-built container for this demo or NGC container

#### Pre-built container

#### NGC Container
Register NGC API Key at https://ngc.nvidia.com/

Log in nvcr.io using API Key
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
xhost +
sudo docker run --gpus all -it --rm --network=host -v $(pwd)/ds-demo:/opt/nvidia/deepstream/deepstream-5.1/ds-demo \
   -v /tmp/.X11-unix:/tmp/.X11-unix -e DISPLAY=:0 -w /opt/nvidia/deepstream/deepstream-5.1 nvcr.io/nvidia/deepstream:5.1-21.02-triton
```

### Usage
After entering container, install jupyter notebook
```
pip install jupyter
```

Host jupyter server and follow the notebook to run your selected demo
```
jupyter notebook --allow-root --ip=0.0.0.0
```

### Technical Support
Contact NVIDIA HK Team for support
