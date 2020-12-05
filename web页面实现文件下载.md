

#### 一、标准URL下载方式：

http get请求，在web页面嵌入url超链接，形如：“http://psctest.cltt.org/qm-hyks-svc/temp/d22b8234-9f5b-474b-9596-78fb6da0b192/信息管理表.xlsx”

具体嵌入方式：

##### 1.window.open()和window.location.herf()

 window.open() 会打开新页面，暴露链接地址，并会在下载文件过程中，访问链接两次，前端下载一次文件，服务端生成两次文件；

  window.location.href 对 浏览器不能打开的文件 可实现下载

##### 2.form表单

##### 3.a标签

##### 4.iframe

##### 5.download.js  

```html
npm install downloadjs 
```





