Steps to use my  Mysql
1. Add below lines in pom.xml
                 <dependency>
                        <groupId>org.springframework.boot</groupId>
                        <artifactId>spring-boot-starter-data-jpa</artifactId>
                </dependency>
                <dependency>
                         <groupId>mysql</groupId>
                         <artifactId>mysql-connector-java</artifactId>
                         <version>8.0.12</version>
                </dependency>
2. Add below lines in application.properties
  # Datasource configuration
spring.datasource.url=jdbc:mysql://localhost:3306/santadb?autoReconnect=true&allowPublicKeyRetrieval=true&useSSL=false
spring.datasource.username=admin
spring.datasource.password=root
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.datasource.initialization-mode=always

# JPA (Hibernate) configuration
spring.jpa.database-platform=org.hibernate.dialect.MySQL5Dialect
spring.jpa.hibernate.ddl-auto=update

3.To view data after insertion 
docker exec -it secretsanta-generator-db-1 mysql -u root -p
USE santadb;
SHOW TABLES;
SELECT * FROM your_table_name;

 
