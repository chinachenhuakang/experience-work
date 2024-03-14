## 1.下载nvm:https://github.com/coreybutler/nvm-windows/releases
## 2.移除本机中的node程序，以及环境变量
	C:\Users{User}\AppData\Roaming\npm
	C:\Users{User}\AppData\Roaming\npm-cache
## 3.配置淘宝镜像
	nvm node_mirror https://npmmirror.com/mirrors/node/
	nvm npm_mirror https://npmmirror.com/mirrors/npm/
## 4.下载node
	nvm install 版本号 eg: nvm install 12.22.10
## 5.查看已安装的node版本
	nvm ls 或 nvm list
## 6.使用指定版本的node
	nvm use 12.22.10
## 7.查看node版本
	node -v
## 常用命令
	nvm ls		#查看已安装的node版本
	nvm install 版本号	#安装指定版本的node
	nvm use 版本号	#切换指定版本
	nvm uninstall 版本号 #卸载指定版本
	nvm list available 	#查看可安装的node版本



### vue-tools 运行
https://github.com/vuejs/devtools
npm install yarn -g
### 下载的devtools包
yarn install
yarn run build:watch & yarn run dev:chrome
