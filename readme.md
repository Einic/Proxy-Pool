# Proxy Pool

爬虫一般情况下需要FQ，请自行修改SPIDER_PROXIES的配置，参考格式：
```
SPIDER_PROXIES = {'http': 'socks5://127.0.0.1:1086', 'https': 'socks5://127.0.0.1:1086'}
```

如果发现新的站点，可以增加SITES的内容

## USAGE 使用方法
安装依赖
```bash
pip3 install requests
```

运行
```bash
python3 Proxies.py

# 指定验证的URL（默认是ip138）
python3 Proxies.py -u 'https://www.baidu.com'

# 指定输出文件位置（默认是proxies.txt）
python3 Proxies.py -o 'output.txt'

# 指定从文件读入代理校验（默认是爬虫爬代理）
python3 Proxies.py -f 'input.txt'

# 从指定文件读取代理，并指定校验网站和输出位置
python3 Proxies.py -f 'input.txt' -u 'https://www.baidu.com' -o 'output.txt'
```

> 注意：输出文件会被覆盖。

