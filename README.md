# vue_node
vue项目的后端，基于node和mongodb
### 此项目为https://github.com/ch634421335/vue_app  项目的后端及管理系统，基于node和mongodb。
# 安装环境
安装node[10-14.5均可]
```
curl --silent --location https://rpm.nodesource.com/setup_12.x | sudo bash -
sudo yum install -y nodejs
检测: node -v
```
安装mongodb
```
//安装mongodb
sudo yum install mongodb-server mongodb -y      //针对centos<8.x

//创建数据库目录和日志目录
mkdir -p /data/mongodb
mkdir -p /data/logs/mongodb

//启动数据库文件存储位置
mongod --fork --dbpath /data/mongodb --logpath /data/logs/mongodb/nodeapp.log
//检测：输入mongo可以进入mongodb，输入 show dbs可以看到当前的数据库
```
导入数据库  
进入mongodb数据库文件夹内  
输入 mongoimport -d app -c 集合 -file 服务器json路径/xx.json 导入一个表  
（例如导入admin：mongoimport -d app -c admin -file ./admin.json）(admin根据几个表名不同进行修改)

安装依赖
输入`npm i`或者`yarn`(根据使用的工具不同自行选择)

# 运行项目
输入`npm start`（使用nodemon运行）  或者node ./bin/www(使用node运行)
如果环境及依赖包安装完整可以看到
 ```
[nodemon] 2.0.4
[nodemon] to restart at any time, enter `rs`
[nodemon] watching path(s): *.*
[nodemon] watching extensions: js,mjs,json
[nodemon] starting `node ./bin/www`
```
在浏览器中输入http://localhost:9001/admin/  
账号密码
alex alex123
admin admin123
heheda heheda123
即可登录到后台。
