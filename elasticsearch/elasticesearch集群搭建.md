### elasticsearch集群安装步骤
#### 1. 安装包下载地址
百度云:**[下载](https://pan.baidu.com/s/1zlEMYBIS6IAvFlcLYl_etA)**  
   
密码:**pvcv**

#### 2. 下载 2.3.1版本
1. elastic安装包
2. ik分词词
3. head插件

#### 3. elasticsearch节点安装
（1）解缩包至安装目录并重命名elasticsearch-2.3.1为**elasticsearch**  
（2）在elasticsearch目录下新建文件夹**plugins**  
（3）解压ik与head插件至新建plugins目录下

#### 4. 授权用户elastic（可自行设置用户名）
```
useradd elastic  // 创建新用户
passwd elastic  // 设置新用户密码
```
#### 5. 修改yml配置
```text
cluster.name: elasticsearch-test（集群名称，自定义名称即可）

node.name: node6（节点名称）
node.master: true（是否是主节点）
node.data: true

network.bind_host: xxx.xx.xx.xx（本机地址）
network.publish_host: xxx.xx.xx.xx（本机地址）

http.port: 9200（http监听端口号）
transport.tcp.port: 9300（tcp端口号）
transport.tcp.compress: true

path.data: /apps/elasticsearch/data（数据存储路径，需要系统挂载在数据分区中）
path.logs: /apps/elasticsearch/logs（日志存储路径）

discovery.zen.minimum_master_nodes: 2
discovery.zen.ping.multicast.enabled: false
discovery.zen.fd.ping_timeout: 10s
discovery.zen.fd.ping_retries: 3
discovery.zen.fd.ping_interval: 60s
# 设置集群节点地址,格式["ip:port"]，多节点以逗号隔开
discovery.zen.ping.unicast.hosts: ["xxx.xx.xx.xx:9300"]

bootstrap.mlockall: true

action.disable_delete_all_indices: true
action.destructive_requires_name: true

# 分词器设置
index.analysis.analyzer.ik.type : "ik"
index.analysis.analyzer.default.type: "ik"
index.number_of_shards: 4
index.number_of_replicas: 1
index.cache.field.type: soft
index.translog.sync_interval: 30s
index.translog.durability: async
index.translog.flush_threshold_size: 4g
index.translog.flush_threshold_ops: 500000

threadpool.search.size: 80
threadpool.search.queue_size: -1
```
#### 6. 启动elastic节点
```
1 新增elastic的文件权限 chown -R elastic /elastic安装路径
2 su elastic
3 cd /elastic安装路径
4 ./bin/elasticsearch -d
```

#### 7. 访问集群
```commandline
http://localhost:9200/_plugin/head/
```