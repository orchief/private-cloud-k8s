## 基于k8s搭建整套私有云集群
1. 服务器资源准备
    1. master服务器两台以上
    2. node服务器2台以上
    3. 监控机一台
2. 网络环境检查
    1. 关闭防火墙或对内网特定ip开放端口
    2. 关闭SELinux
3. 安装k8s-master 2台以上（高可用）
4. 安装k8s-node
5. 将node加入到k8smaster
6. 在监控机部署rancher
7. 在rancher中将集群加入
8. 安装istro，并部署到集群
9. 在rancher安装集群监控工具
10. 搭建集群自动化流水线系统