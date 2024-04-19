# open-mpi-example

Open MPI Cluster example code for a cluster created with [Metafog.io](https://metafog.io)

## Login
SSH Into Metafog Cluster Head Node.

Create a file `my-hostfile.txt` using an editor and put all the IPs of the cluster VMs as below.

```text
100.64.XXX.XXX
100.64.XXX.XXX
100.64.XXX.XXX
```

## MPI Command

Then run the below command to see the hostnames of all the VMs in the cluster.

```bash
$ mpirun --mca oob_tcp_if_include metafog --hostfile my-hostfile.txt  hostname
```

Note: hostname command is not a MPI enabled command but used for testing network handshaking. 
Please refer to [OpenMPI website](https://docs.open-mpi.org/en/v5.0.x/launching-apps/quickstart.html) for MPI enabled samples like hello_c and ping.
