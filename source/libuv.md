---
title: Libuv
tags: ["libuv"]
excerpt: libuv
date: 2020-1-13
---

# [Libuv](https://libuv.org/)


## Install

```sh
$ git clone https://github.com/libuv/libuv.git
$ sh autogen.sh
$ ./configure
$ make
$ make check
$ make install
```

### Hello World
```c
/*
* xlz_test.c
* empty msg loop
* 这个例子新建了一个消息队列，但队列里没有任何消息，程序直接退出
* Created on 2016/9/10
*/

#include <stdio.h>
#include <stdlib.h>
#include "uv.h"

int main(char argc, char *argv[])
{
    uv_loop_t *loop = uv_loop_new();  // 可以理解为新建一个消息队列
    uv_run(loop, UV_RUN_DEFAULT);     // 启动消息队列，UV_RUN_DEFAULT模式下，当消息数为0时，就会退出消息循环。
    printf("hello, world\n");
    return 0;
}
```

### 编译失败
```sh
gcc test.c

/tmp/cc5gugSS.o: In function `main':
test.c:(.text+0x12): undefined reference to `uv_loop_new'
test.c:(.text+0x27): undefined reference to `uv_run'
collect2: error: ld returned 1 exit status
```

```sh
gcc test.c -luv
```
即可
