# grep
Linux系统中grep命令是一种强大的文本搜索工具，它能使用正则表达式搜索文本，并把匹配的行打印出来.  
命令格式：grep [option] pattern file  
-c    --count   #计算符合样式的列数。 
-d <动作>      --directories=<动作>   #当指定要查找的是目录而非文件时，必须使用这项参数，否则grep指令将回报信息并停止动作。   
-l    --file-with-matches   #列出文件内容符合指定的样式的文件名称。  
-n   --line-number   #在显示符合样式的那一行之前，标示出该行的列数编号。   
-r   --recursive   #此参数的效果和指定“-d recurse”参数相同。  
^  #锚定行的开始 如：'^grep'匹配所有以grep开头的行。    
$  #锚定行的结束 如：'grep$'匹配所有以grep结尾的行。    
.  #匹配一个非换行符的字符 如：'gr.p'匹配gr后接一个任意字符，然后是p。    
*  #匹配零个或多个先前字符 如：'*grep'匹配所有一个或多个空格后紧跟grep的行。    
.*   #一起用代表任意字符。   


# ps
Linux ps （英文全拼：process status）命令用于显示当前进程的状态  
ps -A 显示进程信息, 列出所有进程  
ps -ef //显示所有命令，连带命令行

实例：  
查找指定进程：ps -ef|grep svn 查找进程满足命令行中包含svn
查找指定进程个数: ps -ef|grep -c svn  
从文件中读取关键词进行搜索: cat test.txt | grep -f test2.txt----说明：输出test.txt文件中含有从test2.txt文件中读取出的关键词的内容行  
从文件中读取关键词进行搜索 且显示行号： cat test.txt | grep -nf test2.txt
从文件中查找关键词 grep 'linux' test.txt  
输出以hat结尾的行内容： cat test.txt |grep hat$  

