# 操作系统课程设计-文件系统

>
> by Team CodingHero
>


# 功能说明

>
> 下面描述可能未及时更新，请以程序内 `help` 指令输出为准
>

## 基本命令

`login`                     用户登入
`mkdir <newdirname>`        在当前目录下新建目录
`cd <directory>`            进入指定路径
`ls`                        打印当前目录下的内容
`create <filename>`         创建文件
`open <filename> <openmode>`            打开文件
`write <filedescriptor> <txt> <size>`   写入文件
`read <filedescriptor>`                 读取文件内容
`close <filedescriptor>`    关闭文件
`rmfile <filename>`         删除文件
`rmdir <directory>`         删除空目录
`logout`                    用户登出
`format`                    系统格式化
`halt`                      系统保存退出
`help`                      若无额外参数，显示所有的指令及其格式；若有额外参数，则显示指定参数的指令格式及其详细说明

## 测试命令
`pof`           打印所有已打开的文件
`pu`            打印所有用户信息
`psys`          打印超级块信息
`loaddata`      载入样例数据

## 新增功能
`cat <filename>`                将文件内容打印至终端
`chmod <mode> <filename>`       更改权限模式                 
`cp`                            将指定内容复制到指定路径,支持目录到目录的复制
`hardlink <linkedfile> <newfile>`   创建指定文件的硬链接
`symbollink <source> <linkname>`    创建指定源的软链接
`readlink <link>`               读取链接内容
`rmlink <link>`                 删除软链接            
`rename <filename> <newfilename>`   文件重命名
`rm [-r/rf] <path>`             删除路径的指定内容，`[-r/rf]`为可选参数，代表递归删除
`writer <filename>`             编辑指定文件的内容，若文件不存在则直接新建文件
`save <filename> <text> <size>` 将指定文本保存至指定文件内

## 用户相关
`chpasswd`                  修改密码
`urename <username>`        修改指定用户的用户名
`chgroup`                   修改用户所属用户组，仅root用户可操作
`adduser`                   用于添加用户，仅root用户有此权限
`su <username>`             切换到指定用户

## bash命令
`bash <filename>`   用于执行文件内容
`echo <txt>`        直接输出文本内容      



# 图形界面运行方法

## 本地运行

```sh
# 0. 环境准备
# 请确保已安装nodejs
# 1. 进入前端文件夹
cd web
# 2. 安装包管理器yarn
npm install -g yarn
# 3. 自动安装依赖
yarn
# 4. 运行
npm run start
# 5. 访问
http://localhost:4535
```

## 云端运行
1. 将最新代码push到仓库
2. 浏览器访问 http://101.43.158.82:4535
3. 点击更新，等待自动更新
4. 手动刷新网页


# 编译运行与调试方法

## Linux环境

```sh
# 1. 进入代码文件夹
cd os
# 2. 进入构建文件夹
mkdir build # 若不存在请先创建
cd build
# 3. 构建
cmake ..
make
# 4. 运行
./main_d

# 5. 调试
# 修改完代码后，在任意文件界面按下F5开始调试
```


## Windows环境
```sh
# 1. 进入代码文件夹
cd os
# 2. 进入构建文件夹
mkdir build # 若不存在请先创建
cd build
# 3. 构建
cmake .. -G "MinGW Makefiles"
mingw32-make
# 4. 运行
main_d

# 5. 调试
# 修改完代码后，在任意文件界面按下F5开始调试
```

