# Grunt Workflow v1.3

**Grunt Workflow** 是一个基于 [Grunt]的 优雅的、高效的、可定制的前端工作流程

## 快速开始

提供以下三种方式获取：

- [下载最新版 Grunt Workflow](https://github.com/twbs/bootstrap/archive/v3.1.1.zip).
- Clone the repo: `git clone https://github.com/twbs/bootstrap.git`.
- 用 [Bower](http://bower.io) 安装: `bower install bootstrap`.

  阅读 [说明文档](http://getbootstrap.com/getting-started/) 了解更多.

### 文件结构

安装完成后，你会得到如下所示的文件结构：

```
Grunt-Workflow/
│
├── package.json 				// 项目依赖定义
├── Gruntfile.js 				// 配置任务
├── .ftppass 					// FTP 部署密码(非必选)
│
├── html/ 					// HTML文件
│   └── index.html
├── css/ 						// CSS源文件(通常为`Less`/`Sass`等)
│   ├── lib-reset.less
│   ├── lib-mixins.less
│   └── style.less
├── img/ 						// 图片素材 [*非*合并 Sprite(雪碧图)] 如：logo
│   ├── logo.png
│   └── background.png
├── slice/ 						// 图片素材 [待自动合并 Sprite] 如：Icons
│   ├── icon-github.png
│   ├── icon-github@2x.png 		// 含 1x & 2x 图
│   ├── icon-apple.png
│   ├── icon-apple@2x.png
└── publish/ 					// 目标文件夹，存放可发布的成品
    ├── css/ 					// 最终 CSS 成品
    │	└── style.css
    ├── img/ 					// 仅 Copy 不错操作
 	│   ├── logo.png
    │	└── background.png
    └── sprite/ 				// 自动生成的雪碧图
    	└── demo.png



   
```

## 一个完整的Grunt工作流，其中包含Task：
    
* Less编译CSS
* CSSLint检验
* CSS压缩
* 自动合并雪碧图
* 自动处理Retina 2x适配
* 文件变动监控
* FTP发布部署
* Zip打包

## 命令包括：

#### `grunt`  

默认流，输出 publish['css', 'img', 'slice']  
仅Less->CSS，无其他操作  

#### `grunt all`
完全发布流，输出 release['css', 'img', 'sprite']

#### `grunt debug`
调试流，输出 publish['css', 'img', 'sprite']，不清除 [tmp]

#### `grunt push`
将release版本，FTP上传

#### `grunt zip`
将release版本，Zip打包到根目录，命名为`proj-xxx-release.zip`

## 已解决问题

* Mac & Win下的版本下 CPU图片压缩算法不同导致的 版本库Diff问题
* 去除了开发过程中频繁的编译、压缩、合并图片等操作

## 示例图

!11[](http://ww3.sinaimg.cn/large/644eac00gw1e9woj8gddmj20cr0mijuj.jpg)