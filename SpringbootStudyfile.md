# Spring boot study 
## 支持jsp
1.  添加依耐  
          <dependency>
	  <groupId>org.apache.tomcat.embed</groupId>
	  <artifactId>tomcat-embed-jasper</artifactId>
	  <scope>provided</scope>
	  </dependency>
	  <dependency>
	  <groupId>javax.servlet</groupId>
	  <artifactId>jstl</artifactId>
          </dependency>

2.  添加src/main/resources/application.properties内容  
   # 页面默认前缀目录
   spring.mvc.view.prefix=/WEB-INF/jsp/
   # 响应页面默认后缀
   spring.mvc.view.suffix=.jsp
   # 自定义属性，可以在Controller中读取
   application.hello=Hello Shanhy
3.  在 src/main 下面创建 webapp/WEB-INF/jsp 目录用来存放我们的jsp页面   
