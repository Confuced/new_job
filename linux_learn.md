grep命令
zgrep命令 
tail命令 https://www.cnblogs.com/peida/archive/2012/11/07/2758084.html

# 启动
Redirecting to /bin/systemctl start  mariadb.service  
Redirecting to /bin/systemctl stop  mariadb.service  


# 文件的CRUD
- mv 通配符 TARGET_POSITION  
- tar命令的使用: 参考: https://www.cnblogs.com/jyaray/archive/2011/04/30/2033362.html  
高频命令 tar -cf OUTPUT.tar WILDCARD_OR_DIR; tar -xf TO_EXTRACT_TAR.tar; tar -tf TO_EXTRACT_TAR.tar;  

# command
awk 
site: http://www.ruanyifeng.com/blog/2018/11/awk.html  
sed
site: https://www.cnblogs.com/fridge/p/4861888.html  


# 命令的快捷键  
- 根据已有的字符搜索历史命令: 先按ctrl+r, 键入字符, 不停的按ctrl+r翻页, 想要执行就按 enter.  
! 注意, 千万不能先输入字符, 再按ctrl+r, 先按ctrl+r是为了把第一次键入的字符当做关键字符搜索, 如果不输入, 那就默认为空. 根本什么都搜不到.  
  > 这个命令中越是特殊的字符搜索的越快.  

# 网络命令
curl 
参考: 阮一峰的curl教程. http://www.ruanyifeng.com/blog/2011/09/curl.html  


# 环境变量
删除别名的命令 set/unset
- export 和默认的, set, env 有啥区别呢?
参考: https://www.jianshu.com/p/fec33aed017b
set 包含所有. (shell + user) vairables
env: user的. env原本的意思是提供一个 临时改变的环境运行一个命令. 相当于一个虚拟环境. env打印出来的变量是跨shell的.
export: shell -> user.

- source, '.','sh'的区别
source=='.' 把所有变量输出到当前shell, sh(bash)开启子shell, 子shell和父shell变量不通, 自定义临时变量隔离.    
参考: https://www.cnblogs.com/mingziday/p/3262336.html  

- bashrc和bash_profile的区别: 参考:https://www.cnblogs.com/liduanjun/p/3536993.html 
核心观点: profile是个人资料.  登录一次使用一次.


# BashScript
- read 怎么玩?  read -p '' VARIABLE_NAME

# 文本编辑器Vim
- 设置背景颜色 highlight lineNr ctermfg=red
参考: https://blog.csdn.net/ghostyusheng/article/details/53738073

# Others
Linux和Windows的换行符到底什么区别?
在linux上执行脚本时出现$’\r’:command not found,然而仔细检查脚本，对应行位置只是一个空行，并没有问题，那么linux为什么会将一个回车的空行报错？
原因是这样的：脚本是在window下编辑完成后上传到linux上执行的，win下的换行是回车符+换行符，也就是\r\n,而unix下是换行符\n。linux下不识别\r为回车符，所以导致每行的配置都多了个\r，因此是脚本编码的问题。
在linux上执行 dos2unix 脚本名，再次执行脚本，报错消失。

