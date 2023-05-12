# 532 Project
Secure Deep Learning Inference on Trusted Execution Environment. You can run this application with a simulated one by using QEMU.

Hongyu Cai (hongyucai@umass.edu), Zixuan Huang (zixuanhuang@umass.edu)

# Document

Project Proposal: [Secure Deep Learning Inference on Trusted Execution Environment](https://drive.google.com/file/d/1VaW-ZWbQCzQ-p8APoRgQwfEfK1JPamS5/view?usp=sharing)

# Video

Demo Video: [532-Project-Demo Video](https://clipchamp.com/watch/BsWHEm3A36t)

# Run
## Setup OP-TEE
Follow the instruction in "**Get and build the solution**" to build  [the OP-TEE solution](https://optee.readthedocs.io/en/latest/building/gits/build.html#get-and-build-the-solution), and run the below command to start QEMU console.
```
make run
(qemu)c
```

Follow step8 ~ step9 to do unit test. Run:
```
tee-supplicant -d
xtest
```

## Build
```
make run
```

## Inference
By simply typing the following command, you can do inference using a pre-trained model.
```
secdeep classifier predict cfg/mnist.dataset cfg/mnist_lenet.cfg models/mnist/mnist_lenet.weights  data/mnist/images/t_00009_c0.png
```
