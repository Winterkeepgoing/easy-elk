
## 基于docker环境搭建

#### docker-compose.yml
 * 3节点的elasticsearch version 7.5.0
 * kibana version 7.5.0
 * cerebro version 0.8.5
 
#### docker-compose-es-pure.yml
 * 3节点的elasticsearch version 7.5.0
 * [官方文档](https://www.elastic.co/guide/en/elasticsearch/reference/7.5/docker.html)

## 硬件推荐
 Docker至少分配4G的内存
 
## 说明
1. es75_01节点监听 localhost:9200
2. es75_02节点和es75_03节点 通过docker网络elastic和es75_01通信
3. kibana75和es75_01通过docker网络elastic通信
 
### 操作命令

```
# 启动
docker-compose up

# 停止容器
docker-compose down

# 停止容器并且移除数据
docker-compose down -v

# 查看节点的运行情况
curl -X GET "localhost:9200/_cat/nodes?v&pretty"
```


