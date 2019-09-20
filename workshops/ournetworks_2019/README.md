# Collaboratively backing up IPFS content with IPFS Cluster

These is the information page for the IPFS Cluster workshop at the
[OurNetworks 2019 Conference](https://ournetworks.ca/program/#collaboratively-backing-up-ipfs-content-with).

* **Location**: Gamma Workshop Space
* **Date**: Sunday 22/9 at 14:00h.

## Workshop agenda

This will be an hands-on workshop: we will form a local IPFS Cluster, add and
pin content to multiple IPFS daemons and explain the general architecture of a
Cluster.

## Installation instructions

IPFS Cluster provides two command-line tools:

* `ipfs-cluster-service` to run the cluster peer (daemon)
* `ipfs-cluster-ctl` to interact with it, add pins etc.

### For skilled Go users (build and install)

0. Start your `ipfs` daemon and:

```shell
git clone git@github.com:ipfs/ipfs-cluster.git;
cd ipfs-cluster;
git checkout v0.11.0;
make install;
```

### For others (download pre-compiled binaries)

Please follow the following instructions to install and configure your cluster
for the workshop:

0. Start your `ipfs` daemon (with the terminal or with IPFS Desktop should be ok).
1. Create a `cluster-workshop` and download the following files in it.
1. Download `ipfs-cluster-service`:
   1. For Mac download: https://dist.ipfs.io/ipfs-cluster-service/v0.11.0/ipfs-cluster-service_v0.11.0_darwin-amd64.tar.gz
   2. For Linux download: https://dist.ipfs.io/ipfs-cluster-service/v0.11.0/ipfs-cluster-service_v0.11.0_linux-amd64.tar.gz
   3. For Windows download: https://dist.ipfs.io/ipfs-cluster-service/v0.11.0/ipfs-cluster-service_v0.11.0_windows-amd64.zip
   4. For other platforms check: http://dist.ipfs.io/ipfs-cluster-service/v0.11.0

2. Similarly, download `ipfs-cluster-ctl`:
   1. For Mac download: https://dist.ipfs.io/ipfs-cluster-ctl/v0.11.0/ipfs-cluster-ctl_v0.11.0_darwin-amd64.tar.gz
   2. For Linux download: https://dist.ipfs.io/ipfs-cluster-ctl/v0.11.0/ipfs-cluster-ctl_v0.11.0_linux-amd64.tar.gz
   3. For Windows download: https://dist.ipfs.io/ipfs-cluster-ctl/v0.11.0/ipfs-cluster-ctl_v0.11.0_windows-amd64.zip
   4. For other platforms check: http://dist.ipfs.io/ipfs-cluster-ctl/v0.11.0

3. Extract the downloaded `tar.gz` or `zip` files in a `cluster-workshop` folder (i.e. `tar -xf <file>`). You should endup with something like:

```
cluster-workshop/
 ipfs-cluster-ctl
    ipfs-cluster-ctl
    LICENSE
    README.md
 ipfs-cluster-ctl_v0.11.0_linux-amd64.tar.gz
 ipfs-cluster-service
    ipfs-cluster-service
    LICENSE
    README.md
 ipfs-cluster-service_v0.11.0_linux-amd64.tar.gz

2 directories, 8 files
```

4. Open two terminal windows:
   1. Use one to navigate to the `ipfs-cluster-ctl` folder. i.e. `cd cluster-workshop/ipfs-cluster-ctl`.
   2. The second one to navigate to the `ipfs-cluster-service` folder. i.e. `cd cluster-workshop/ipfs-cluster-service`.


## Starting the Cluster

(For people downloading to a folder, prepend commands with `./` (for example `./ipfs-cluster-service`)

1. Run `ipfs-cluster-service init http://localhost:8080/ipns/workshop.cluster.ipfs.io` (make sure ipfs is running)
2. Run `ipfs-cluster-service daemon`
3. Watch the logs and switch to your other shell to get started with `ipfs-cluster-ctl`!
