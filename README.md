# 备份网站到七牛
好处：七牛可以免费10G备份资源
作为个人网站，或小型企业，是一个不错的选择

# 依赖
* qshell [下载](https://github.com/qiniu/qshell)
* zip


# 配置
1. 下载七牛qshell工具
2. 拷贝config.ini.backup为config.ini
3. 按照说明修改配置

# 使用
```bash
sudo chmod +x backup.sh
./backup.sh
```

# 定时备份
```bash
crontab -e

# 填入以下,每天凌晨两点执行一次备份,这里可以根据活跃度进行调整
0 2 * * * /bin/bash /foo/backup.sh

# 我这边网站不活跃，这里配置成每月备份一次
* * * 1 * /bin/bash /foo/backup.sh
```

# 更新说明
* [issue-#1](https://github.com/Ecareyu/backup2qiniu/issues/1) 增加子目录配置项,为空时获取服务器hostname作为子目录名

# 参考
[backuptoqiniu](https://github.com/ccbikai/backuptoqiniu)
