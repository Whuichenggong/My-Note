---
date: 2024-12-23
aliases:
  - 别名功能
tags:
  - demo
---

1. ctrl + ；

2. [[]]链接到其他笔记 

出链查看链接 跳转连接功能

反向链接： 第二篇笔记在第一篇笔记中引用了他 它可以查看到谁引用了他

引用和被引用！

3.  ctrl + p


我今天创建了[[]]


图标格式 

| 系统调用               | 描述                                   |
|-----------------------|--------------------------------------|
| `fork()`              | 创建进程                               |
| `exit()`              | 结束当前进程                           |
| `wait()`              | 等待子进程结束                         |
| `kill(pid)`           | 结束 pid 所指进程                      |
| `getpid()`            | 获得当前进程 pid                       |
| `sleep(n)`            | 睡眠 n 秒                              |
| `exec(filename, *argv)` | 加载并执行一个文件                    |
| `sbrk(n)`             | 为进程内存空间增加 n 字节              |
| `open(filename, flags)` | 打开文件，flags 指定读/写模式         |
| `read(fd, buf, n)`    | 从文件中读 n 个字节到 buf              |
| `write(fd, buf, n)`   | 从 buf 中写 n 个字节到文件             |
| `close(fd)`           | 关闭打开的 fd                         |
| `dup(fd)`             | 复制 fd                               |
| `pipe(p)`             | 创建管道，并把读和写的 fd 返回到 p     |
| `chdir(dirname)`      | 改变当前目录                           |
| `mkdir(dirname)`      | 创建新的目录                           |
| `mknod(name, major, minor)` | 创建设备文件                   |
| `fstat(fd)`           | 返回文件信息                           |
| `link(f1, f2)`        | 给 f1 创建一个新名字(f2)               |
| `unlink(filename)`    | 删除文件                               |

1. **表格语法**：
    
    - 使用 `|` 分隔列。
        
    - 使用 `-` 分隔表头和内容。
        
    - 对齐方式可以通过 `:` 调整（例如 `:---` 左对齐，`:---:` 居中对齐，`---:` 右对齐）。
        
2. **代码格式**：
    
    - 使用反引号 `` ` `` 将代码（如函数名）包裹起来，以显示为等宽字体。
        
3. **Obsidian 支持**：
    
    - Obsidian 完全支持 Markdown 表格语法，可以直接粘贴上述代码到 Obsidian 中查看效果。