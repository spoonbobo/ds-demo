## Deepstream Demos

### Prerequisites

Pull DeepStream-demo image
```
docker pull spoonnvidia/ds-demo:peoplenet-v1
```

Create DeepStream-demo Container
```
xhost +
docker run --gpus all -it --rm --network=host -v /tmp/.X11-unix:/tmp/.X11-unix -e DISPLAY=:0 \
   -w /opt/nvidia/deepstream/deepstream-5.1 spoonnvidia/ds-demo:peoplenet-v1
```

### Usage
After entering container, host jupyter server and follow the notebook to run your selected demo
```
cd ds-demo/notebook
jupyter notebook --allow-root --ip=0.0.0.0
```

### Technical Support
Contact NVIDIA HK Team for support
