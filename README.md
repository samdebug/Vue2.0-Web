# vue2.0与express(https://h5.m.taobao.com/app/movie/pages/index/index.html?from=def&spm=a1z2r.7661912.h5-movie-list.121&sqm=a1z2r.7661912.1.1&bottomtab=show)页面

## 描述
项目中加入一个server服务，模拟服务器环境，为前端提供数据来源，当用`npm run deploy`命令运行前端环境时，就可以直接将前端资源部署到server服务里。因此本项目有两个环境，一个是前端开发环境(端口是8080)，一个是server服务环境(端口是9090)。

主要技术栈：<br/>
- vue2.0
- vue-router
- vuex
- mint-ui
- nodejs
- express
	
## 如何运行
下载项目
```
 git clone https://github.com/canfoo/vue2.0-taopiaopiao.git
```
 打开一个终端（称这个终端为A终端）进入到vue2.0-taopiaopiao目录安装依赖包
```
 npm install
```
 打开另一个一个终端（称这个终端为B终端）进入到server目录安装依赖包
```
 npm install
```
启动server服务（得先启动后台服务，否则前端页面没有数据），在server目录下执行以下命令，成功执行会终端会提示服务端口号为9090
```
 npm run start
```
启动前端开发服务，在vue2.0-taopiaopiao目录里执行以下命令，成功执行后，会自动打开浏览器访问前端开发环境，浏览地址是`http://localhost:8080`
```
 npm run dev
```
前端资源部署到server里，开发完成后，在vue2.0-taopiaopiao目录里执行以下命令，成功执行后，可以通过访问server提供的路径访问到页面了，访问路径为`http://localhost:9090/app`
```
 npm run deploy
```

备注：因为本项目有提供后台服务，所以当前端部署到服务器后，只要后台服务启动，就可以直接通过`http://localhost:9090/app`路径访问到前端页面，无须再启动前端的开发服务。


## 主要目录结构
> build  
> config <br/>
> src  //前端主要开发目录<br/>
>  --assets  //存放前端静态资源<br/>
>  --components  //存放组件<br/>
>  --store  //vuex数据流管理<br/>
>  --views  //页面试图，由vue-router引入<br/>
>  --App.vue <br/>
>  --main.js  //前端入口文件<br/>
>server  //后台服务<br/>
>  --bin  //启动后台服务配置<br/>
>  --database  //存放页面所需要的json数据<br/>
>  --public  //前端部署时存放在后台服务的位置<br/>
>  --routes  //路由于请求接口管理<br/>
>  --views  //前端模板存放位置<br/>
>  --app.js  //后台服务入口<br/>
	
