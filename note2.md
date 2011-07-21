#第二部分 program C
##apply for vim
###编译gcc（cc）
     gcc -Wall a.c      #调试

     echo $?            #测试系统的返回值

     vim 下直接回到 bash 使用 ：sh    恢复到vim 用ctrl_d
    (此光标保持不变 修改之后需保存方可调试)

###vim中使用Tab补全 功能

 (the substance of install the vim plugin is that put plugin behind /home/akaedu )

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

then  we can use that set



