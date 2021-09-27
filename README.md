# idcard

身份证验证

area.json 更新于 [2020年中华人民共和国行政区划代码](http://www.mca.gov.cn/article/sj/xzqh/1980/202105/20210500033655.shtml)

# 安装

```bash
$ go get -u github.com/guanguans/id-validator
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