## CHtask3
Chalmers University Task #3

### Task description
[Firecracker](https://github.com/firecracker-microvm/firecracker) is one of the coolest new technologies in computer systems today. It allows you to spin-up a VM in less than 500ms,  even faster than a container. In this task, your task is to start and run a machine learning inference model of your choice on a firecracker VM. You will then run docker locally on your computer and deploy the same model in a docker container.. You will then benchmark the performance of the algorithm, focusing on how the underlying system affects the performance of model-serving. Please note, we only care about CPU performance now with no need to consider GPUs.

# Note

The model was a simple classification model on an EEG dataset, since it was not the objective of the task. The objective was to see how a ML model will be served on Docker and Firecracker.
If it will be necessary to choose a more complex model, please let me know and I will change it.

Also, the Firecracker was running a CenOS. The etx and the kernel size were too huge and I decided not to include them in the repository to make the cloning of the repository quicker since the firecracker can also be run on any OS possible. If you need me to include them as well, Please let me know.

# Time and CPU% comparison of the inference model

The process of how I received these numbers are discussed in the pdf report file. I have also included a package named "Scalene" in the Dockerfile. which can be used to graphically profile the memory pefromance of the inference code. The usage of the Scalene is as easy as "scalene inference.py".

Here is the [Scalene](https://github.com/plasma-umass/scalene) repository for more information.

![Time and CPU%](https://user-images.githubusercontent.com/56083377/208298707-06474a19-4b47-4cb1-9d9b-15dd99927823.jpg)
