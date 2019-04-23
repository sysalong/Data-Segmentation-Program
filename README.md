# Data-Segmentation-Program
txt 自定义数据分割程序

这里描述一下程序的主要作用，程序总共两个功能。

详细说明参考：https://woj.app/5133.html

txt数据处理程序：
这里描述一下程序的主要作用，程序总共两个功能。
程序内每步也都有提示，一定一定一定要看。


【功能一】（数据分类保存）：

把要分类的txt文件放入程序同目录下daichuli文件夹(自行建立)，

这里举例，txt内容可以是(中间分割符必须统一，要么是----要么是&&&&，分隔符随便，但是必须所有txt文件的分隔符必须统一)::

账号 ---- 密码

asdfasdf123 ---- ffff123456

asdf@asdf.com ---- 12312

asdf@qq.com ---- abcdef123

程序会把 全数组的密码保存为一类txt，把全英文的一类保存为一类txt，会把英文数组混合一类保存为txt。

保存至程序同目录下1log文件夹内。




【功能二】（取账号数字、英文与密码混合）：

把要分类的txt文件放入程序同目录下1log文件夹(自行建立)，

例如下面的数据：

asdfasdf123 ---- ffff123456

asdf@asdf.com ---- 12312

asdf@qq.com ---- abcdef123

程序处理后会保存在2log文件夹内。变为如下格式（取账号的英文放置在数字密码前面；取账号的数字放置纯英文密码的后面）：

asdfasdf123 ---- asdfasdffff123456

asdf@asdf.com ---- asdf12312

asdf@qq.com ---- asdfabcdef123




【功能三】（取账号数字、英文与密码混合）：

把要分类的txt文件放入程序同目录下1log文件夹(自行建立)，

例如下面的数据(功能三下1、2小项都是同等替换部管位置)：

asdfasdf123 ---- ffff123bbb456

asdf@asdf.com ---- 12312

asdf@qq.com ---- abcdef123cc123

asdf@qq.com ---- 4444abc555

程序处理后会保存在3log文件夹内。变为如下格式（取账号前面的字母或数字替换密码里面的英文或字母）：

asdfasdf123 ---- asdfasdf123bbb456

asdf@qq.com ---- asdf123cc123

asdf@qq.com ---- 4444asdf555

-----------------------------------------------------------

↑↑↑例如下面的数据(功能三下3、4小项都是替换后，字母在前)：注意和上面的区别↑↑↑

asdfasdf123 ---- ffff123bbb456

asdf@asdf.com ---- 12312

asdf@qq.com ---- abcdef123cc123

asdf@qq.com ---- 4444abc555

程序处理后会保存在3log文件夹内。变为如下格式（取账号前面的字母或数字替换密码里面的英文或字母）：

asdfasdf123 ---- asdfasdf123bbb456

asdf@qq.com ---- asdf123cc123

asdf@qq.com ---- asdf4444555             ←←←注意这个与上面的区别是3、4小项的特点。






【程序在win10下无错运行】

如果程序报错，提示缺少api-ms-win-crt-process-l1-1-0.dll 等问题，

你需要安装以下两个微软补丁： 

https://support.microsoft.com/zh-cn/help/3118401/update-for-universal-c-runtime-in-windows

https://support.microsoft.com/zh-cn/help/2999226/update-for-universal-c-runtime-in-windows

找到自己系统对应的下载安装后再运行即可。



安装上面两个补丁有个先决条件： 
要安装此更新，您必须在Windows 8.1或Windows Server 2012 R2中安装Windows RT 8.1，Windows 8.1和Windows Server 2012 R2（2919355）① 的2014年4月更新汇总。或者，安装适用于Windows 7或Windows Server 2008 R2的Service Pack 1②。或者，安装适用于Windows Vista和Windows Server 2008的Service Pack 2。

说白了，你需要选择下面你对应的系统，去安装这个补丁，安装完下面的补丁，然后再安装上面那两个你系统对应的补丁： 

下载基于Windows 7 和 Windows Server 2008 R2 Service Pack 1 的文档 (KB976932) https://www.microsoft.com/zh-cn/download/details.aspx?id=269

下载基于x86的Windows 8.1更新包。http://www.microsoft.com/downloads/details.aspx?familyid=47b21d89-3f78-477f-9402-8021e61bef59

下载基于x64的Windows 8.1更新包。http://www.microsoft.com/downloads/details.aspx?familyid=f2917221-a8b3-4024-b755-818ad0e7703d

下载基于x64的Windows Server 2012 R2更新包。http://www.microsoft.com/downloads/details.aspx?familyid=373b1bb0-6d55-462e-98b7-6cb7d9ef1448

下载基于Windows Vista和Windows Server 2008 Service Pack 2(自己看吧，这两个系统较为复杂)
 https://support.microsoft.com/en-us/help/948465/information-about-service-pack-2-for-windows-vista-and-for-windows-ser


作者：龍哥 博客：https://woj.app
