# idcard

身份证验证

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
	idcard.Init("./area.json")
	fmt.Println(idcard.Check("xxxxxxxxxxxxxxxxxx"))
}
```