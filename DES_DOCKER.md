[【部署后遇到问题】](http://www.webfunny.cn/website/faq.html) | [【自定义警报配置】](http://www.webfunny.cn/website/api.html) |  正常情况下，1个小时以后出分析数据，不要着急

### Docker部署方式

运维部署非我强项，我这里只能提供方法，仅供参考。

1. 项目内我增加了dockerfile, 想使用docker部署版, 请自行打包image文件。

2. image文件打包方法，请参考[docker入门 阮一峰](http://www.ruanyifeng.com/blog/2018/02/docker-tutorial.html)。

3. 监控系统会使用两个端口号：8010、8011 ;

注意事项：所以生成容器的时候也需要映射两个端口号出来，例如： docker container run -p 8010:8010 -p 8011:8011 -it webfunny_monitor /bin/bash
