# 需求文档
## 前端
前端使用react 生成一个页面,页面有个按钮点击触发get请求后端接口传参是id=1，h1title
页面显示绿色h1标题的文字，文字内容是接口返回的json数据的title内容
## 后端
后端使用go语言接收h1title请求返回title:a 内容的json对象,其中a是查询mysql数据库content表title字段的值;

## 数据库
mysql地址是localhost:3306,库是test,表是content,查询字段是title
设计mysql库表，content表有id和title两个字段，通过mysql链接工具执行语句创建库表和mock数据

@/docs/product.md 根据需求在src下分别创建react前端项目front_web,后端项目api_service,并生成对应代码，在mysql中创建对应库表和mock数据