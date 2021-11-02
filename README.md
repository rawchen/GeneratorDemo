# SpringBoot自动代码生成器

## 增删改查模糊查询分页 - 后端零代码

### 使用方式

1. MySQL新建一张或多张表，含有**id**字段（int且自增主键）、**create_time**字段（datetime）、**update_time**字段（datetime），最好所有字段都加上个中文注释。

2. 新建SpringBoot项目，Maven引入以下依赖，最最下面。（parent为2.x.x以上）

3. 复制该项目中的**base包**，也就是base文件夹到你的**主启动类同路径位置**，正确修改**base包中所有类的首行包路径**。

4. 打开base包中**GeneratorUtil**类，修改必须修改的**参数**（表数组，包路径，数据库连接参数）。

5. 运行GeneratorUtil类中**main**方法即可。

6. 复制资源文件夹中的**application.yml**，修改数据库连接参数，端口号，项目名等，mapper接口路径（用来打印sql语句日志）。

7. 可以复制**config文件夹**到主启动类同路径位置，即可访问**localhost:端口号/swagger-ui.html**，测试CRUD分页模糊查询了。

### 截图预览

![](https://cdn.jsdelivr.net/gh/rawchen/JsDelivr/static/GeneratorDemo/01.png)

![](https://cdn.jsdelivr.net/gh/rawchen/JsDelivr/static/GeneratorDemo/02.png)

![](https://cdn.jsdelivr.net/gh/rawchen/JsDelivr/static/GeneratorDemo/03.png)

### Maven：
```xml
   <dependency>
   	<groupId>org.springframework.boot</groupId>
   	<artifactId>spring-boot-starter</artifactId>
   </dependency>
   <dependency>
   	<groupId>org.springframework.boot</groupId>
   	<artifactId>spring-boot-starter-web</artifactId>
   </dependency>
   <dependency>
   	<groupId>org.springframework.boot</groupId>
   	<artifactId>spring-boot-starter-test</artifactId>
   	<scope>test</scope>
   </dependency>
   <!-- 必须 -->
   <dependency>
   	<groupId>mysql</groupId>
   	<artifactId>mysql-connector-java</artifactId>
   	<version>8.0.25</version>
   </dependency>
   <dependency>
   	<groupId>org.mybatis.spring.boot</groupId>
   	<artifactId>mybatis-spring-boot-starter</artifactId
   	<version>1.3.3</version>
   </dependency>
   <dependency>
   	<groupId>io.springfox</groupId>
   	<artifactId>springfox-swagger2</artifactId>
   	<version>2.8.0</version>
   </dependency>
   <dependency>
   	<groupId>io.springfox</groupId>
   	<artifactId>springfox-swagger-ui</artifactId>
   	<version>2.8.0</version>
   </dependency>
   <dependency>
   	<groupId>org.apache.commons</groupId>
   	<artifactId>commons-lang3</artifactId>
   	<version>3.11</version>
   </dependency>
   <dependency>
   	<groupId>com.alibaba</groupId>
   	<artifactId>druid</artifactId>
   	<version>1.2.8</version>
   </dependency>
```