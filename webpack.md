#### 静态资源打包：

##### 	静态资源种类：

​	js(.js  .jsx  .coffee中间语言  .ts中间语言)

​	css(.css .less .sass . scss) less和scss的用法

​	Images （.jpg .png .gif .bmp .svg ）

​	字体文件（Fonts）(.svg .ttf .eot .woff .woff2)

​	模板文件 (.ejs .jade .vue)



##### 	静态资源引入问题：

​	网页加载速度慢，发起多次二次请求

​	处理复杂的依赖关系

​	问题解决：

1. 合并、压缩、精灵图、图片的base64编码

2. requireJS或使用webpack，解决包之间复杂依赖关系

   ##### 如何完美实现上述解决方案：

   1. 使用Gulp,基于task任务

   2. 使用Webpack，基于整个项目进行构建

      

##### 	安装webpack:

​	

​	webpack能处理JS文件的相互依赖

​	webpack能处理浏览器兼容问题