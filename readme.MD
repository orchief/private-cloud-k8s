## 基于k8s搭建整套私有云集群
1. 服务器资源准备
    1. master服务器三台 (实现物理隔离)
    2. node服务器2台以上 按需扩展
    3. LB(Master/Backup)	192.168.0.137	Nginx L4
    4. rancher监控机一台
2. 网络环境检查
    1. 关闭防火墙或对内网特定ip开放端口
    2. 关闭SELinux
3. 谷歌服务器国内无法正常访问问题处理办法
    1. 收集需要下载的镜像仓库
    2. 创建对应的github仓库（私有仓库也可以例如自建gitlab）
    3. 使用阿里云镜像服务， 关联对应仓库， 注意要勾选海外机构构建
    4. 构建对应阿里云的镜像
    5. 使用image.sh脚本下载并重新tag对应镜像
3. 安装k8s-master 2台以上（高可用）
4. 安装k8s-node
5. 将node加入到k8smaster
6. 在监控机部署rancher
7. 在rancher中将集群加入
8. 安装istro，并部署到集群
9. 在rancher安装集群监控工具
10. springcloud项目docker化，docker-compose编排
11. docker-compose编排 转换成 k8s部署配置文件 https://github.com/kubernetes/kompose/releases/tag/v1.24.0
11. springcloud项目 docker-compose编排 部署到k8s集群
10. eureka k8s 日志统一管理
10. 搭建集群自动化流水线系统
11. 项目运维功能发布工作流程
12. springcloud JVM监控
13. APM链路跟踪
14. 基于HPA的峰值弹性伸缩