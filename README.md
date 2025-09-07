第一步  修改UUID后直接部署到cf works；
第二步  绑定自定义域名
第三步  打开V2RayN——添加vless配置文件——用户名随便写 地址写优选ip  端口 443系  80系都可以   uuid填写你设置的    伪装域名和sni填写你的自定义域名   传输协议ws
第四步 重点：！！！！路径填写方式  /?mode=direct   直连  无法访问cf网站  
                               /?mode=s5&s5=user:pass@host:port    仅SOCKS5
                               /?mode=auto&direct&s5=user:pass@host:port（直连优先，回退SOCKS5）
/?mode=auto&direct&proxyip=host:port    直连优先，回退ProxyIP
/?mode=auto&s5=user:pass@host:port&proxyip=host:port    SOCKS5优先，回退ProxyIP
/?mode=auto&proxyip=host:port&s5=user:pass@host:port     ProxyIP优先，回退SOCKS5
/?mode=auto&direct&s5=user:pass@host:port&proxyip=host:port     三者都有：直连→SOCKS5→ProxyIP 
/?mode=auto&s5=user:pass@host:port&proxyip=host:port&direct    三者都有：SOCKS5→ProxyIP→直连 
/?mode=auto&proxyip=host:port&s5=user:pass@host:port&direct     三者都有：ProxyIP→SOCKS5→直连 
