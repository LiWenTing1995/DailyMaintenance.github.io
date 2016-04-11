# Linux日常运维指令和脚本
------
### case 1：shell终端for循环
```bash
usage:
    for i in {1..10};do step1; step 2; step 3; done
sample:
    for i in ./*; do echo $i; echo `basename $i`; done
```    

### case 2：crontab任务计划
```
usage:
    -l：查看计划清单
    -e：编辑计划清单
    -d：删除计划清单
example:
    * 1/* * * * cp file1 file2
```

### case 3：shell字符截断
```
usage:
    -#：顺序截断第一个
    -##：顺序截断最长的一个
    -%：逆序截断第一个
    -%%：逆序截断最长的一个
example:
    dir = /home/xx/zsrc/libtiff/tools/.libs
    echo ${dir##*/} 获取文件路径，等同于dirname $dir
    echo ${dir%/*}  获取文件名，等同于basename $dir
```
