# 切片append之后，为什么一次添加3个以上的值时，容量会比长度大

```
package main

import "fmt"

func main() {
  var s []int
  printSlice(s)

  // 可以一次性添加多个元素
  s = append(s, 2, 3)
  printSlice(s)

  // 可以一次性添加多个元素
  s = append(s, 2, 3, 4)
  printSlice(s)
}

func printSlice(s []int) {
  fmt.Printf("len=%d cap=%d %v\n", len(s), cap(s), s)
}

// len=0 cap=0 []
// len=2 cap=2 [2 3]
// len=5 cap=6 [2 3 2 3 4] // 为什么容量是6
```

# go web

