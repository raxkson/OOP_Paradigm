# 2020년도 1학기 객체지향 패러다임 개인 프로젝트
### 도서 대출, 반납 등의 기본적인 도서관리를 위한 웹페이지입니다.
## Server
- OS: Ubuntu Server 18.04LTS - 개인서버
- Server: Tomcat(Docker)
- DB: MySQL(Docker)
- SSL: letsencrypt
- URL: https://test.oseonsik.com/library

## 기술스택
- Apache Tomcat/8.5.53
- JSP&Java Servlet
- HTML
- JavaScript
- CSS
- BOOTSTRAP
- Docker
- python(DB에 데이터를 채우기 위해)

## DB 구조
- ### 회원관리 
  - Purpose: 회원가입한 사용자를 저장하기 위함
  - Table name: members
  -  | Field     | Type        | Null | Key | Default | Extra          |
     |:----------|:------------|:-----|:----|:--------|:---------------|
     | id        | int         | NO   | PRI | NULL    | auto_increment |
     | user_name | varchar(45) | NO   |     | NULL    |                |
     | user_id   | varchar(45) | NO   | UNI | NULL    |                |
     | passwd    | varchar(65) | NO   |     | NULL    |                |
     | stu_num   | int         | NO   |     | NULL    |                |
     | phone     | varchar(45) | NO   |     | NULL    |                |
     | mail      | varchar(45) | NO   |     | NULL    |                |
     
- ### 도서관리
  - Purpose: 보관중인 도서를 저장하기 위함
  - Table name: booksinfo
  - | Field    | Type         | Null | Key | Default | Extra          |
    |:---------|:-------------|:-----|:----|:--------|:---------------|
    | id       | int          | NO   | PRI | NULL    | auto_increment |
    | name     | varchar(500) | NO   |     | NULL    |                |
    | writer   | varchar(100) | YES  |     | NULL    |                |
    | price    | int          | NO   |     | NULL    |                |
    | rent     | tinyint      | NO   |     | 1       |                |
    | rent_num | int          | NO   |     | 0       |                |
    | rent_by  | varchar(45)  | YES  |     | NULL    |                |
    