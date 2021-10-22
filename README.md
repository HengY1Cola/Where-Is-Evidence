#  数字取证

##  Wp

- [2020长安杯Wp pro]()
- [2019长安杯Wp pro]()

##  必要的命令

###  查询文件/夹

- whereis只能用于程序名的搜索。
- find命令

```bash
# 这里着重说一下find命令
# 当前目录搜索所有文件，文件内容 包含 “140.206.111.111” 的内容
find . -type f -name "*" | xargs grep "140.206.111.111"

# 在/home目录下查找以.txt结尾的文件名
find /home -name "*.txt"

# 匹配文件路径或者文件
find /usr/ -path "*local*"

# 搜索恰好在七天前被访问过的所有文件
find . -type f -atime 7

# 搜索大于10KB的文件
find . -type f -size +10k

# 删除 mac 下自动生成的文件
find ./ -name '__MACOSX' -depth -exec rm -rf {} \;

# 统计代码行数,排除空行
find . -name "*.java"|xargs cat|grep -v ^$|wc -l
```

###  查看/筛选文件夹

- grep命令

```bash
# 在多个文件中查找：
grep "match_pattern" file_1 file_2 file_3 ...

# 统计文件或者文本中包含匹配字符串的行数 -c 选项：
grep -c "text" file_name
cat file_name | grep "text" -n
```

> cat：从第一行开始显示文本内容（适用于内容较少的）
> tac：从最后一行开始显示，是 cat 的逆顺序
> more：一页一页的显示文本内容（适用于内容较多的）
> less：与 more 类似，但是比 more 更好的是，它可以往前翻页！
> head：只看文本的前面几行
> tail：只看文本的后面几行
> nl：显示文本内容与行号

- cat命令

> - Ctrl + s 停止滚屏幕
> - Ctrl + q 恢复滚动
> - Ctrl + c 中断

- more命令

> - Enter 向下翻一行
> - 空格 向下滚动一屏幕
> - Q 退出命令

- less命令

> PageUp 向上翻
>
> PageDown 向下翻
>
> Q 退出

###  查询历史

- history命令

```bash
# 使用history命令显示最近使用的10条历史命令
history 10

选项
-c           清空历史列表。
-d offset    根据offset删除记录。如果是正数则表示offset位置的记录，如果为负数则表示从结尾向前offset位置的记录。
-a           将当前终端的历史记录行添加到历史记录文件。
-n           将尚未从历史文件中读取的历史行追加到当前历史列表中。
-r           读取历史文件，并将其内容附加到历史列表中。
-w           将当前历史记录列表附加到历史记录文件中并且附加它们到历史列表中。
-p           在每个arg上执行历史记录扩展并在标准输出上显示结果，而不将结果存储在历史记录列表中。
-s           将每个arg作为单个条目附加到历史记录列表。

# ⚠️注意：
在命令行中，可以使用符号!执行指定序号的历史命令。例如，要执行第2个历史命令，则输入!2。
关闭终端后，历史列表将被写入历史文件~/.bash_history。
环境变量HISTSIZE决定了历史文件中命令的存储数量，默认存储1000条。
```

##  工具🔧

###  火眼手机

说明书链接🔗

###  火眼仿真

说明书链接🔗







