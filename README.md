# run-dns

# DNS的坑

## 1、ping缓慢
  ping的第一个包缓慢，后续正常。通过是strace监控到域名解析缓慢。需要换dns server，或者暂时本地host增加域名解析。

## 2、ssh登录缓慢
  sshd机器打开IP验证。需要调用dns功能。如果ssh客户端机器的IP并无域名，则需要等待dns解析超时（测试约20秒），才会登录成功。

