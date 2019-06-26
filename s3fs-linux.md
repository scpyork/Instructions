# How to mount the s3 browser to your local machine

This is similar for MacOS, except the installation instructions. 


## Install

```
sudo apt-get install s3fs

less | man s3fs
```


## Add credentials
```
echo <ACCESS_KEY>:<SECRET_KEY> ~/.passwd-s3fs


```

## Mount unmount
```
mkdir [directory]

echo "mount"
echo "s3fs [bucketname] [directory] -ouse_cache=/tmp -o allow_other"

echo "unmount"
echo "fusermount -u [directory]"
```
## Mount (read only)
```
s3fs [bucket] [dir]-o umask=0222 -o ro

```
