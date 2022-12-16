# MNIST Example in Apptainer (PyTorch version)
This classic example of hand-written text recognition is well suited both as a lightweight test when learning FEDn and developing on FEDn in psedo-distributed mode. A normal high-end laptop or a workstation should be able to sustain a few clients. 

## Prerequisites
- [Ubuntu 20.04](https://releases.ubuntu.com/20.04)
- [Apptainer](https://apptainer.org/)

## Running the example in a fully-distributed FEDn cluster
To start and remotely connect a client with the required dependencies for this example, start by modifying configuration files in 
`config/extra_hosts` and `settings-client.yaml`. 

Then you can build the Apptainer image for FEDn clients
```
bin/1-build_client
```

Then, get the computing package from the as-built Apptainer image
```
bin/2-get_compute_package
```

The next command splits the data in 6 parts for the clients.
```
bin/3-split_data
```

Now you are ready to start the client.

```bash
bin/4-start_clients
```
