# Simple Blog

成员：

* 马易颜 17343085
* 林国梁 17343073

### 项目介绍

该项目简单的设计了一个博客网站的前端与后端，所用到的技术与思想包括：

* **API FIRST**：先创建博客服务与外部交互的文档API，然后再根据API来开发代码
* **REST** 风格API
* **Open API specification**：利用yaml规格完成API的具体设计
* **Swagger editor + Swagger UI**：利用Swagger的web editor将设计的API 可视化
* **Swagger codegen**：根据设计好的Open API 自动创建go-server与javascript client
* **boltDB**： 采用基于key-value存储的数据库高效存取数据

### 文件结构



### API风格

采用REST 风格的API

...

### Swagger editor + Swagger UI

通过在线的[Swagger web editor](https://swagger.io/tools/swagger-editor/f)进入到**live demo**后，导入`swagger.yaml`即可将API可视化，并在线编辑：

![](./images/1.png)

### Swagger codegen

该工具可以利用写好的API yaml文件自动创建多种语言的server和client模版，简化开发流程。

* 依赖：java 8以上

* 通过`Wget https://oss.sonatype.org/content/repositories/releases/io/swagger/swagger-codegen-cli/2.2.1/swagger-codegen-cli-2.2.1.jar`下载
* `java -jar swagger-codegen-cli-2.2.1.jar generate -i swagger.json -l go-server`可以创建对应API的go-server
* `java -jar swagger-codegen-cli-2.2.1.jar generate -i swagger.json -l javascript`可以创建对应API的javascript client

