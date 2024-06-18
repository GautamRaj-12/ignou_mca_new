# Spring MVC with Bootstrap CSS

## Configuration of Bootstrap in Spring Application
- Bootstrap is a *free, popular and open-source CSS framework* directed at responsive, mobile-first front-end web development.
- It contains HTML and CSS based design templates for various interface components such as typography, forms, buttons, 
modals, image carousels, navigation etc., as well as optional JavaScript extensions.

### Features of Bootstrap
- **Browser Support**:- Bootstrap supports all popular web browsers such as Chrome, Safari, Firefox, Opera, and Internet edge.
- **Responsive Design**:- Bootstrap enables us to write responsive websites very easily. Its responsive CSS adjusts automatically to Desktops, Tablets and Mobiles.
- **Uniform solution to build interface**: Bootstrap provides a clean and uniform solution to build an interface for the developers. 
- **Customization:** Bootstrap provides a simple and easy way to customize the CSS.
- **Functional built-in components**: Bootstrap contains beautiful and functional built-in components which can be customized very easily.

## Different ways to configure bootstrap

### 1. Bootstrap through Content Delivery Network(CDN)
- CSS: Copy-paste the below Stylesheet link to the `<head>` tag of your desired HTML/JSP file. 
```
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384‐
EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC"crossorigin="anonymous">
``` 
- JS: Place the following `<script>`s near the end of your pages, right before the closing `</body>` tag.
```
<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.2/dist/umd/popper.min.js" integrity="sha384‐IQsoLXl5PILFhosVNubq5LC7Qb9DXgDA9i+tQ8Zj3iwWAwPtgFTxbJ8NT4GN1R8p" crossorigin="anonymous"></script>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.min.js" integrity="sha384‐cVKIPhGWiC2Al4uLWgxfKTRIcfu0JTxR+EQDz/bgldoEyl4H0zUF0QKbrJ0EcQF" crossorigin="anonymous"></script>
```

### 2. Custom configuration of Bootstrap with Spring MVC (Offline by downloading files locally)
- Download the bootstrap css and js files from Bootstrap website.
- Put static resources CSS and JS files into `webapp/resources/static` directory. To segregate CSS and JS, keep them into respective folders `webapp/resources/static/css` and `webapp/resources/static/js`.
- Create the resource mapping into Spring using either **XML configuration** or  **Java Configuration**
  - **XML configuration**
    ```
    <mvc:resources mapping="/js/**" location="/resources/static/js/" />
    <mvc:resources mapping="/css/**" location="/resources/static/j=css/" />
    ```
  - **Java Configuration**
    ```
    @Configuration 
    @EnableWebMvc 
    public class MyApplication implements WebMvcConfigurer 
    { 
        public void addResourceHandlers(final ResourceHandlerRegistry registry) 
        { 
            registry.addResourceHandler("/js/**").addResourceLocations("/resources/static/js/"); 
            registry.addResourceHandler("/css/**").addResourceLocations("/resources/static/css/"); 
        } 
    }
    ```
- Include the Bootstrap CSS and JS into JSP page via **JSTL tag** ***c:url*** or **Spring tag** ***spring:url***. 
    - **JSTL tag *c:url***
    ```
    <%@taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %> 
    <!DOCTYPE html> 
    <html lang="en"> 
        <head> 
            <link href="<c:url value="/css/bootstrap.css" />" rel="stylesheet"> 
            <script src="<c:url value="/js/jquery.1.10.2.min.js" />"></script> 
            <script src="<c:url value="/js/bootstrap.js" />"></script> 
        </head> 
        <body> 
        </body> 
    </html>
    ```
    - **Spring tag *spring:url***
    ```
    <%@ taglib prefix="spring" uri="http://www.springframework.org/tags"%> 
    <!DOCTYPE html> 
    <html lang="en"> 
        <head> 
            <spring:url value="/css/bootstrap.css" var="bootstrapCss" /> 
            <spring:url value="/js/jquery.1.10.2.min.js" var="jqueryJs" /> 
            <spring:url value="/js/bootstrap.js" var="bootstrapJs" /> 
            <link href="${bootstrapCss}" rel="stylesheet" /> 
            <script src="${jqueryJs}"></script> 
            <script src="${bootstrapJs}"></script> 
        </head> 
        <body>
        </body> 
    </html>
    ```
## Apply custom CSS in Pages
- **Css for just one page**
```
<head> 
    <style type="text/css"> 
        p { 
            color: green; 
        } 
    </style> 
</head> 
<body> 
    <p> 
    This is Green Color Text. 
    </p> 
    <p> 
    This is another paragraph with a green color. 
    </p> 
</body>
```
- **custom css**
```
<link rel="stylesheet" type="text/css" href="css/custom.css">
```

## Create, Read, Update, Delete (CRUD)
- The acronym CRUD stands for CREATE, READ, UPDATE and DELETE. The CRUD paradigm is common in constructing web applications. While constructing the APIs, the model should provide four basic types of functionality such as Create, Read, Update and Delete the resources. CRUD operations are also often used with SQL. 

### EXample of CRUD
- **Create**: A new student is entered into the database.
- **Read**: The student's information is displayed to the users.
- **Update**: Already, existing student’s attributes are being updated with new values.
- **Delete**: If the student is not part of the institute, the student can be deleted from the records. 

### Mapping CRUD to SQL statements

- This table provides examples of SQL statements for performing Create, Read, Update, and Delete (CRUD) operations on a `student` table.

| Function | Operation | SQL Statement |
|----------|------------|---------------|
| Create   | Insert     | `INSERT INTO student (name, grade) VALUES ('Prasoon', 10);` |
| Read     | Select     | `SELECT * FROM student;` |
| Update   | Update     | `UPDATE student SET grade = 10 WHERE id = 1;` |
| Delete   | Delete     | `DELETE FROM student WHERE id = 1;` |

### Mapping CRUD to REST
- In REST context, CRUD corresponds to Rest web service POST, GET, PUT and DELETE respectively. The following table maps CRUD to REST with example. 

| Function | Operation | HTTP Method | Endpoint URL                           |
|----------|------------|-------------|----------------------------------------|
| Create   | POST       | `POST`      | `http://teststudent.com/students/`     |
| Read     | GET        | `GET`       | `http://teststudent.com/students/`     |
| Update   | PUT        | `PUT`       | `http://teststudent.com/students/1`    |
| Delete   | DELETE     | `DELETE`    | `http://teststudent.com/students/1`    |

### CREATE
- To create a resource in a REST environment, HTTP Post method is used. Post method creates a new resource of the specified resource type. To create a new student record for the Student Management System, HTTP POST request and response are shown below. 
  - **REQUEST**:POST http://teststudent.com/students/
  - **REQUEST BODY**:
    ```
    { 
    "firstName": "Anurag", 
    "lastName": "Singh", 
    "grade": 10 
    }
    ```
  -  **RESPONSE:** Status Code – 201(Created)
    ```
    { 
        "id": 1, 
        "firstName": "Anurag", 
        "lastName": "Singh", 
        "grade": 10 
    } 
    ```