# elasticsearch  

##filebeat

```
> https://github.com/s1ckdark/elasticsearch.git

> tar -xvzf filebeat-7.15.0-darwin-x86_64.tar.gz   

> mv filebeat-7.15.0-darwin-x86_64 filebeat

> cd filebeat 

> cp ../filebeat-eslog.yml ./filebeat-eslog.yml
# yml의 owner는 root여야만함
> sudo chown root filebeat-eslog.yml

> sudo ./filebeat -e -c filebeat-eslog.yml


```

##elasticsearch
```
> docker-compose -f docker-compose-cluster.yml up -d
> curl http://127.0.0.1:9200/_nodes/process?pretty=true
> curl http://localhost:9200/_cat/nodes?format=json&pretty
```

##kibana
```
> docker-compose -f docker-compose-kibana.yml up -d
```

