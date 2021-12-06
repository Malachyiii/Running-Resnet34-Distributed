# Running-Resnet34-Distributed

This repository is an exploration of running a Resnet34 neural network on a single AWS instance vs. on two AWS instances using PyTorch distributed training.

## Containerization

In both the distributed and non-distributed examples, the NVIDIA PyTorch AMI was used as the base image for the AWS Instance. Jupyter Notebooks was then installed on the instance.

In order to run the notebooks, the container must be started with --network host and access to the gpus. To run the distributed training, the instances must be created in the same
security group with the appropriate ports open on both instances.

## Running the Notebooks in tandem

In order to run the distributed training, ssh into both instances in separate terminals, and start up the appropriate notebooks. Run all in the notebook on the main machine which will
pause when it reaches cell 8, at which point it will pause and wait for the second machine. Run all on the second notebook. You can now watch the progress on Weights and Biases.
