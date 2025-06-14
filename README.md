REST API - Spring Boot
Các bước thực hiện
dự án Spring Boot cung cấp REST API để quản lý người dùng  
- Đăng ký, chỉnh sửa, xóa mềm (soft delete)
- Xác thực (authentication) & phân quyền (authorization) USER & ADMIN (chỉ cho phép admin được thêm sửa xóa xem user 
- Sử dụng MySQL làm cơ sở dữ liệu 
Yêu cầu môi trường
- Java 17+  
- Maven 3.6+  
- MySQL 8.x  
- Postman 

 1. Tạo dự án trên 
  https://start.spring.io/
 - Spring Web
- Spring Data JPA
- Spring Security
- Lombok
- MySQL Driver
2. Tạo database
CREATE DATABASE shop;

3. Cấu hình kết nối trong src/main/resources/application.properties
spring.application.name=testRestApi
server.port=1111
spring.datasource.url=jdbc:mysql://localhost:3306/shop?useSSL=false&serverTimezone=UTC&allowPublicKeyRetrieval=true
spring.datasource.username=root
spring.datasource.password=root

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect

4 tạo Entity 
5 tạo Reposity
6 Tạo Security
7 Tạo service 
8 SecurityConfig
9 Tạo controller

10 tạo trước dữ liệu trong MySQL

INSERT INTO users (
    id, name, username, password, email,
    phone, avatar, status, role, deleted
) VALUES (
    32, 
    'Nguyen Van A', 
    'ad2', 
    '$2a$10$IfWOJlASyKQ/jvTgwWMWwuqVa52BnLRguK7pXHJOwhv6cv/mG5ona', 
    'ad2@gmail.com', 
    '0123456789', 
    'link-anh.jpg', 
    true, 
    'ADMIN', 
    false
);

11 chạy project 
