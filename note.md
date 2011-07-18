## git

## install
 （下载）

   sudo apt-get install git-core 

   sudo apt-get install tig
 
   git clone + 网页 only-read 地址  
 
   git pull   更新网页内容
 
   查看用 tig 看加入的内容 d
                                                                            

## git basic
    
    mkdir www           建立新的文件夹
 
    cd www             
    
    ls       
    
    ls -a               查看隐藏文件
    
    vim hello           建立新的vim
    
    git add hello       跟踪hello 文件(注：如果第二次修改可不用此命令)
    
    git commit -a -m "first"       修改一次过的信息后 设置留言的名字 即“first”
    （-a 即 all   -m 即 message）
    
    tig                            查看修改的内容
    
    history 10                    查看此终端的用过的十个命令

## 找两个文件差异
 
   1， 建立新的文件eg:h.c   并 拷贝到文件 eg:h1.c  修改h1.c 的内容

   2，diff -u h.c h1.c                    可直接列出两文件中的多的部分
   
   3，diff -u h.c h1.c > h.diff           即将两文件中的不同 保存到文件h.diff
 
### 补丁  patch
 
 1 ,加补丁    patch h.c < h.diff        即 将h1.c中多的部分加到h.c 中去
 
 2，减补丁    patch -R h.c < h.diff     （其中 “R”  即reverse 相反）

# 关于github.com上Create a Repository

## global setup:

###Set up git        
    （在vim 中建立自己的用户名）
   
   git config --global user.name "sept"
   
   git config --global user.email jfsgj@163.com

###Next steps:    
     
      mkdir sept-note

      cd sept-note                      （可 查看 隐藏文件中 是否有.git）
     
      git init                          （如果没有 加入 .git）
      
      git add note.md                   （增加跟踪文件 note.md）
   
      git commit -m '+留言信息'
     
      git remote add origin git@github.com:sept/sept-note.git   
    
      git push -u origin master

__注__:如果在文件中更新 新的内容字后 git commit -a -m "+留言信息"
                        然后 使用    git push  直接上传至网页即可			           
## vim

    Command = operator + number + motion
                d(elete)  1,2
                y(ank)             gg+G

       其中   小写u还原上一次操作 大写U是恢复原始即全部撤销
              小写p粘贴在光标的下一行 大写P粘贴再光标的上一行

### 注：在vim中 粘贴或进行别的操作时  一定先点i 后可输入


###vim 中
   若非正常关闭或文件正在打开状态中 则此文件的目录名下会多出隐藏文件
   （如：note.md.swp）即 以.swp格式的隐藏文件 
   关闭后 若还有 使用rm -rf 强制删除即可
###vim中 添加行号
   即 ～ vim .vimrc  中输入 set number 即可
   删除行号 即set hidden          
					   
## linux basic
 
  Linux is OS(operating system)
 
  OS as linus see it:
 
  OS is nothing but the kernel.
 
  Linux is nothing but the kernel.
 
  ubuntu is Linux + 1000 app.
 
  OS as MS see it:
 
  OS is kernel + desktop env.

## tips

   Clear screen : Ctrl-l

   Copy and Paste: select -> middle button

## language

  https://github.com/happypeter/job-akae/wiki

## translation

  http://dict.youdao.com/

## shell ( shell is a commandline interpreter)

  bash is a kind of shell. 

## filesystem tree

    ls

    cd 
### ~ means your home dir

   cd .. # go to the parent of current dir

    pwd

    man pwd # q to quit

    mkdir dir

### path

    绝对路径: start with /
    相对路径: start with .

### shell prompt

    peter@cow:~/tg-note$
   
   user@machinename:currentWorkingDirectory(folder)$

### software installation

    sudo apt-get install tree


## tar 

  http://www.happypeter.org/posts/10

## ref

  http://happypeter.github.com/LGCB/

  http://billie66.github.com/TLCL/book/

## 使用复制
   即 cp  目录名的时候 必须加  -r（cp -r ** **）

## 使用markdown 

  (基于 html语言之上的 精简格式)

  2 在vim 下 创建一个新的  .md格式的文件 

  3 然后 用firebox  .md（即网页打开的形式打开笔记）

  4  markdown note.md >note.html    (即将.md转化.html)
     firefox note.html              （）
     vim note.md  
  
  5 其中： 输入 代码时前面打几个空格

  6  内容顶格输入

## 快速查找

  (vim下)  输入 / 后加需要的关键字  

  查找下一出n 查找上一处N

  网页上 输入同上  查找ctrl g/G

  恢复操作 git throw

