## 安装
可以通过运行以下命令安装最新的 Metrics Server 版本：
```shell
kubectl apply -f https://github.com/bococ/metrics-server/blob/main/components.yaml
```
## 注意部署 metrics-server 出现 no metrics known for node
```shell
- args:
        - --cert-dir=/tmp
        - --secure-port=443
        - --kubelet-preferred-address-types=InternalIP,ExternalIP,Hostname
        - --kubelet-use-node-status-port
        - --kubelet-insecure-tls  ## 不添加 - --kubelet-insecure-tls 参数，就会出现   x509  x509  x509 问题 验证问题
        - --metric-resolution=15s
```
