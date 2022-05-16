# idcard

身份证验证

# area.json 来源

area合并于 [中华人民共各国民政部官网数据](http://www.mca.gov.cn/article/sj/xzqh/1980/)

[2011年12月中华人民共和国县以上行政区划代码](http://www.mca.gov.cn/article/sj/tjbz/a/201713/201707271552.html)

[2012年12月中华人民共和国县以上行政区划代码](http://www.mca.gov.cn/article/sj/tjbz/a/201713/201707271556.html)

[2013年12月中华人民共和国县以上行政区划代码](http://files2.mca.gov.cn/cws/201404/20140404125552372.htm)

[2014年12月中华人民共和国县以上行政区划代码](http://files2.mca.gov.cn/cws/201502/20150225163817214.html)

[2015年12月中华人民共和国县以上行政区划代码](http://www.mca.gov.cn/article/sj/tjbz/a/2015/201706011127.html)

[2016年12月中华人民共和国县以上行政区划代码](http://www.mca.gov.cn/article/sj/xzqh/1980/201705/201705311652.html)

[2017年12月中华人民共和国县以上行政区划代码](http://www.mca.gov.cn/article/sj/xzqh/1980/201803/201803131454.html)

[2018年12月中华人民共和国县以上行政区划代码](http://www.mca.gov.cn/article/sj/xzqh/1980/201903/201903011447.html)

[2019年12月中华人民共和国县以上行政区划代码](http://www.mca.gov.cn/article/sj/xzqh/1980/2019/202002281436.html)

[2020年12月中华人民共和国县以上行政区划代码](http://www.mca.gov.cn/article/sj/xzqh/2020/20201201.html)

# 安装

```bash
$ go get -u github.com/zngw/idcard
```

# 使用

先将项目中的area.json复制到工程资源目录

```go
package main

import (
	"fmt"
	"github.com/zngw/idcard"
)

func main()  {
    // 加载本地json数据
	idcard.Init("./area.json")
    // 加载网络配置
    // idcard.Init("")
	fmt.Println(idcard.Check("xxxxxxxxxxxxxxxxxx"))
}
```
