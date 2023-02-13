# Zeek

Analyse a pcap from the docker instance:
```
docker pull zeek/zeek:latest
docker run -v $(pwd):/data -w /data/ -it zeek/zeek /usr/local/zeek/bin/zeek -r /data/FILE
```
