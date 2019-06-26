

```
sudo apt-get install s3fs

less | man s3fs

echo <ACCESS_KEY>:<SECRET_KEY> ~/.passwd-s3fs

mkdir [directory]

echo "mount"
echo "s3fs [bucketname] [directory] -ouse_cache=/tmp -o allow_other"

echo "unmount"
echo "fusermount -u [directory]"

# If you have write access you may ommit the -o ro option (read only)

s3fs [bucket] [dir]-o umask=0222 -o ro

```
