
## pull
```
docker pull winfed/bsdiff4
```
## run
```
docker run --name bsdiff4 \
--restart=unless-stopped \
-v /etc/localtime:/etc/localtime:ro \
-v /data:/data \
-it winfed/bsdiff4
```

## exe
```
// bsdiff：bsdiff oldfile newfile patchfile
docker exec bsdiff4 bsdiff /data/old.txt /data/new.txt /data/diff.patch
// bspatch：bspatch oldfile newfile patchfile
docker exec bsdiff4 bspatch /data/old.txt /data/new.txt /data/diff.patch
```
