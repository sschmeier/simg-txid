# Singularity config for simg-txid container

A [Singularity Hub](https://www.singularity-hub.org/) definition for txid workflow.

If [Singularity](http://singularity.lbl.gov) is installed locally, the container can be build (needs root access) locally like this:

```bash
sudo singularity build simg-txid.simg Singularity > build.log 2>&1
```

The container can alos be downloaded from [Singularity Hub](https://www.singularity-hub.org/) without root access to the local machine like this:

```bash
singularity pull --name "simg-txid.simg" sschmeier/simg-txid:latest 
```

Then, it can be used, e.g.:

```bash
singularity exec simg-txid.simg samtools view -h

# test R
singularity exec --bind /mnt/disk1/seb simg-txid.simg Rscript test.R > session.txt
```
