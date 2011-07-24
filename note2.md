#The part of program C
##apply for vim
###编译(compiling)gcc（cc）
     gcc -Wall a.c      #调试

     echo $?            #测试系统的返回值

     vim 下直接回到 bash 使用 ：sh    恢复到vim 用ctrl_d
    (此光标保持不变 修改之后需保存方可调试)

###vim中使用Tab补全 功能
(the substance of install the vim plugin is that put plugin behind /home/akaedu )
      
       download the snipmate.zip

       unzip snipmate.zip -d ~/.vim

       cd .vim/snippets

       vim c.snippet

       eg: (input) # added for test
                     
		     snippet dog

		    (Tab)    i love dog

###set bash
(use 'aaa' instead 'sudo apt-get' to install sth)     
     ~$ vim .bashrc

     input  on the last line:

     #alias for apt-get

     alias aaa='sudo apt-get'

then close the bash and open bash again

     or  ~$ source .bashrc 

then  we can use that setting
###set vim
(set <tab> equal 4 whitespace)
    set autoindent   ”自动缩进“
    
    set expandtab    “把<tab>展开成空格”
    
    set tabstop=4    “让<tab>占四个空格”

    set shiftwidth=4   “用 '>' 同样占四个空格”

    set dictionary=/usr/share/dict/words  "使用 <ctrl-x-k> 查找单词; 使用 <ctrl-x-f> 查找目录文件名"

    map ,ss =set spell <cr>    "set spell under file or annotation(注释) in the vim"
    
    map <Tab> :bn<cr>           

    imap jj <Esc>          "在插入模式下 use 'jj' to instead <Esc>"

after setting that close the vim , we can use them after open it again
###use <ctrl-t>  <ctrl-d> under insert mode to aligning(对齐) the line 

###check the IP

      (input) ifconfig
###log in others computer

install openssh

        sudo apt-get install openssh-server

connect a computer with its user and IP address

        ssh peter@193.**.**.**

exist from connect

        logout  or <ctrl-d>

__copy__others file or directory:
        
        scp peter@**.**.**:~/h.c .  "copy h.c to my currentdirctory"

stop or start to connect two computer

        sudo service ssh stop/start       "stop/start others log in"

### ctags

    install ctags

    ctrl-]    #from call to  definition    

    ctrl-t    #回到跳转前的位置 

    ctags *   +多个文件    
### The help of vim
        
        (input) vim

search under ordinary mode  
      
       :h o    

search under insert mode

       :h i_ctrl_d

      (or use "h c" knock <Tab>)
## ldd

http://tldp.org/HOWTO/Program-Library-HOWTO/
