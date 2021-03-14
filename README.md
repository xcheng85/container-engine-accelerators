# Hardware Accelerators in GKE

This repository is a collection of installation recipes and integration utilities for consuming Hardware Accelerators in Google Kubernetes Engine.

This is not an official Google product.

More details on the nvidia-gpu-device-plugin are [here](cmd/nvidia_gpu/README.md).

The official instructions for using GPUs on GKE are
[here](https://cloud.google.com/kubernetes-engine/docs/how-to/gpus).




## Notes from Xiao Cheng
nvidia_gpu.go 

Define mount paths

ctor NewNvidiaGPUManager

check device path (wait for nvidia driver installation)

nvml init (nvidia management library for checking states of devices)


//The plugin registers itself with the kubelet through the Unix socket at host path /var/lib/kubelet/device-plugins/kubelet.sock.

// The name of its Unix socket.

//glog.Infof("starting device-plugin server at: %s\n", pluginEndpointPath)

gpumanager serve

// create a new grpc server

// register aplha and beta to the kubelet

// launch the grpc server async

ngm.grpcServer.Serve(lis)

RegisterWithKubelet

RegisterWithV1Beta1Kubelet
