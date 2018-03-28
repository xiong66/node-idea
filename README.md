# node-idea
最近在自己做一个koa+MongoDB+antd的项目。随便写写。

1、MongoDB win环境(win10)安装过程 （ubuntu简单一些，装完了没记录）
  网上 安装教程挺多的，好多都是直接复制的，大佬的是mac环境居多，我也写下我的win环境的。
  官网安装教程：https://docs.mongodb.com/v3.4/tutorial/install-mongodb-on-windows/

  1.1、先去官网下载msi安装文件，我的下载地址：
    https://www.mongodb.com/dr/fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.4.14-signed.msi/download
  1.2、直接打开安装，我选择了默认路径 
    路径：C:\Program Files\MongoDB\Server\3.4
  1.3、然后在安装盘（我是c盘）根目录下 创建data文件夹，和在data文件夹下 创建db文件夹和log文件夹
     ![mongodb_1图片](https://github.com/xiong66/node-idea/master/img/mongodb_1.png)
  1.4、再在mongodb的安装的文件夹下创建 mongo.config文件（需要管理员权限） 
     ![mongodb_2图片](https://github.com/xiong66/node-idea/master/img/mongodb_2.png)
     文件里面的内容为：
     systemLog:
        destination: file
        path: c:\data\log\mongod.log
    storage:
        dbPath: c:\data\db
  1.5、打开cmd命令行（一定要管理员权限打开）
    "C:\Program Files\MongoDB\Server\3.4\bin\mongod.exe" --config "C:\Program Files\MongoDB\Server\3.4\mongod.cfg" --install
    直接copy，回车运行。
    ![mongodb_3图片](https://github.com/xiong66/node-idea/master/img/mongodb_3.png)
  1.6、大功告成，启动 net start MongoDB，关闭 net stop MongoDB
    ![mongodb_3图片](https://github.com/xiong66/node-idea/master/img/mongodb_4.png)