# Java Server Pages

## What are Java Server Pages?
- In Java, JSP stands for Java Server Pages. It is a server-side technology which is used for creating web applications. 
- It is used to create dynamic web content. JSP consists of both HTML tags and JSP tags. 
- In this, JSP tags are used to insert JAVA code into HTML pages. It is an advanced version of Servlet Technology i.e. a web-based technology that helps us to create dynamic and platform-independent web pages. 
- In this, Java code can be inserted in HTML/ XML pages or both. JSP is first converted into a servlet by the JSP container before processing the client’s request. 
- JSP has various features like JSP Expressions, JSP tags, JSP Expression Language, etc.

## JSP Life Cycle

### Transalation and Compilation
- When a JSP is first accessed, it is translated into a corresponding servlet (Java class) and compiled. The translation process is handled by the JSP engine of the underlying web container (e.g., Tomcat). The resulting servlet is then executed to handle incoming requests.

### JSP Life Cycle Methods
- The life cycle of a JSP is controlled by three methods: ***jspInit()***, ***_jspService()***, and ***jspDestroy()***.
- ***jspInit()***
  - **Purpose**: The jspInit() method is called only once during the life cycle of a JSP. Similar to the init() method in servlets, it is used to initialize objects and variables that persist throughout the life cycle of the JSP.
  - **Interface**:Defined in the JspPage interface
  - **Signature**:`public void jspInit() { // Initialization code }`
  - Invoked when the JSP page is initialized.
  - Takes no parameters, returns no value, and throws no exceptions.
- ***_jspService() Method***
  - **Purpose**: The _jspService() method is called every time the JSP page is requested to serve a request.
    Corresponds to the body of the JSP page and should not be redefined by developers.
  - **Interface**:Defined in the javax.servlet.jsp.HttpJspPage interface.
  - **Signature**:
    ```
    public void _jspService(javax.servlet.http.HttpServletRequest request, javax.servlet.http.HttpServletResponse response) throws javax.servlet.ServletException, java.io.IOException {
            // services handling code
        }
    ```
  - Takes HttpServletRequest and HttpServletResponse objects as parameters.
  - Returns no value
- ***jspDestroy() Method***
  - **Purpose**: The jspDestroy() method is invoked only once when the JSP page is about to be terminated. Similar to the destroy() method in servlets. Used for cleanup tasks, such as releasing database connections or closing open files.Corresponds to the body of the JSP page and should not be redefined by developers.
  - **Interface**:
  - **Signature**:`public void jspDestroy() { // cleanup code }`
  - Should be overridden if cleanup tasks are necessary.

![jsp-life-cycle](images/jsp-life-cycle-o.png)

## JSP API
- JSP technology relies on the JSP API (Application Programming Interface).
- Two primary packages are used: **javax.servlet.jsp** and **javax.servlet.jsp.tagext**.
- Additionally, servlet packages are required: **javax.servlet** and **javax.servlet.http**.

- Package **javax.servlet.jsp**:  The javax.servlet.jsp package has two interfaces such as
HttpJspPage and JspPage and four classes such as JspEngineInfo, JspFactory, JspWriter and
PageContext.
- Package **javax.servlet.jsp.tagext**: The javax.servlet.jsp.tagext encompasses classes and
interfaces for the definition of JSP Tag Libraries.The interfaces
in the javax.servlet.jsp.tagext package are BodyTag, IterationTag, Tag, and TryCatchFinally.
The classes are defined in this package such as BodyContent, BodyTagSupport, PageData,
TagAttributeInfo, TagData, TagExtraInfo, TagInfo, TagLibraryInfo, TagLibraryValidator,
TagSupport, TagvariableInfo and VariableInfo

| Interface/Class  | Description                                                                                                    |
|------------------|----------------------------------------------------------------------------------------------------------------|
| **JspPage**      | The JspPage is the interface that all JSP servlet classes must implement. The JspPage interface has two methods, `JspInit` and `JspDestroy`. The `jspInit` method is similar to the `init` method in the `javax.servlet.Servlet` interface. The `jspDestroy` method is analogous to the `destroy` method of the `javax.servlet.Servlet` interface. JSP developers rarely make full use of these two methods.                        |
| **HttpJspPage**  | The HttpJspPage interface directly extends the JspPage interface. Each JSP page implements this interface. It supports only one method `_jspService()`. The `_jspService()` method is already described in the life cycle of JSP in section 4.3 of this Unit.                        |
| **JspEngineInfo**| The JspEngineInfo is an abstract class that provides information on the current JSP engine.                                                      |
| **JspFactory**   | The JspFactory is an abstract class that defines a number of factory methods available to a JSP page at runtime for the purposes of creating instances of various interfaces and classes used to support the JSP implementation.                      |
| **JspWriter**    | The JspWriter class is derived from the `java.io.Writer` class. This is the normal mechanism for JSP pages to produce output to the response. A number of methods are defined in this class such as `print()` and `println()`.                        |
| **PageContext**  | The PageContext class is an abstract class. It extends JspContext to provide useful context information when JSP technology is used in a servlet environment. This class provides methods that are used to create other objects. For example, `getServletConfig()` returns a `ServletConfig` object and `getServletContext()` returns a `ServletContext` object.            |
| **JspException** | The JspException is the base class for all JSP exceptions.                                                                                      |
| **JspError**     | The JspError class is defined in the `javax.servlet.jsp` package of the JSP API.                                                                  |

## Components of JSP
- There are three types of JSP components: **1. Directives**, **2. Scripting**, **3. Action**

## 1. Directives in JSP
- Directives guide the JSP container for translating and compilation of JSP page.
- It appears at the top of the page. Using directives, the container translates a JSP page into the 
corresponding servlet.
- Directives are defined by using `<%@` and `%>` tags.
- Syntax: `<%@ directive attribute = "value" %>`
- There are three types of directive tag −
  
    (i) `<%@ page ... %>` : Defines page-dependent attributes, such as scripting language, error page, and buffering requirements.

    (ii) `<%@ include ... %>`: Includes a file during the translation phase.

    (iii) `<%@ taglib ... %>`: Declares a tag library, containing custom actions, used in the page

### (i) The Page Directive
- The page directive is used to provide instructions to the container. These instructions pertain to the current JSP page. You may code page directives anywhere in your JSP page. By convention, page directives are coded at the top of the JSP page.
- Syntax:
  `<%@ page attribute = "value" %>`
- **Attributes**

| S.No | Attribute         | Purpose                                                                                   |
|------|-------------------|-------------------------------------------------------------------------------------------|
| 1    | buffer            | Specifies a buffering model for the output stream.                                        |
| 2    | autoFlush         | Controls the behavior of the servlet output buffer.                                       |
| 3    | contentType       | Defines the character encoding scheme.                                                    |
| 4    | errorPage         | Defines the URL of another JSP that reports on Java unchecked runtime exceptions.         |
| 5    | isErrorPage       | Indicates if this JSP page is a URL specified by another JSP page's errorPage attribute.  |
| 6    | extends           | Specifies a superclass that the generated servlet must extend.                            |
| 7    | import            | Specifies a list of packages or classes for use in the JSP as the Java import statement does for Java classes. |
| 8    | info              | Defines a string that can be accessed with the servlet's getServletInfo() method.         |
| 9    | isThreadSafe      | Defines the threading model for the generated servlet.                                    |
| 10   | language          | Defines the programming language used in the JSP page.                                    |
| 11   | session           | Specifies whether or not the JSP page participates in HTTP sessions.                      |
| 12   | isELIgnored       | Specifies whether or not the EL expression within the JSP page will be ignored.           |
| 13   | isScriptingEnabled| Determines if the scripting elements are allowed for use.                                 |

- Example :
  ```
  <%@ page import=”java.io.*, java.util.Date” buffer=”16k” autoFlush=”false” % > 
  <%@ page errorPage=”error.jsp” %> 
  ```

### (ii) The Include Directive
- JSP include directive is used to include files such as HTML, JSP into the current JSP document at the translation time. It means that it enables you to import the content of another static file into a current JSP page. The advantage of using an include directive is to take advantage of code re-usability. This directive can appear anywhere in a JSP document.
- Syntax: 
  `<%@ include file = "relative url" >`
- The filename in the include directive is actually a relative URL. If you just specify a filename with no associated path, the JSP compiler assumes that the file is in the same directory as your JSP.
- Example: 
  
  `header.html`

  ```
  <html> 
    <body> 
        <h4>The text is from Header File</h4> 
    </body>
  </html>
  ```
  `index.jsp`

  ```
  <html> 
    <body> 
        <h4>Example of include directive</h4> 
        <%@ include file= "header.html" %>
    </body>
  </html>
  ```
  **Output:** *localhost:8080/exampleproject/index.jsp*
  ```
  Example of include directive
  The text is from Header File
  ```
### (iii) The Taglib Directive
- This directive allows users to use Custom tags in JSP. 
- A custom tag is **user-defined tag**. The custom tag eliminates the need for scriptlet tag.
- Syntax:
  `<%@ taglib uri=”tagLibraryURI” prefix=”tagPrefix” %>`

## 2. Scripting Elements in JSP
- JSP scripting elements is a mechanism for ***embedding java code fragments*** directly into a HTML page.
- There are three scripting language elements such as 
  
  (i) **declarations**: To declare the variables and methods for the page.
  (ii) **expressions**: To return a value from the scripting code as String to the page.
  (iii) **scriptlets**: To execute java source code.

### (i) Declarations
- Declarations are used ***to declare the variables and methods*** that we can use in the JSP document.
- The declaration part is initialized when the JSP document is initialized.
- After the declarations have been initialized, they are available to other expressions,declarations and scriptlets.
- Syntax: 
  `<%! declaration %>`
- Example:
  
  **Declaring variable**

  ```
  <html>  
    <body>  
        <%! int data=50; %>  
        <%= "Value of the variable is:"+data %>  
    </body>  
  </html>  
  ```

  **Declaring Methods**

  ```
  <html>  
    <body>  
        <%!   
            int cube(int n){  
                return n*n*n*;  
            }  
        %>  
        <%= "Cube of 3 is:"+cube(3) %>  
    </body>  
    </html>  
  ```

### (ii) Expressions
- The code placed within JSP expression tag is **written to the output stream of the response.** So you need not write out.print() to write data. It is mainly used to print the values of variable or method.
- Syntax: 
  `<%=  statement %>`
- ***Do not end your statement with semicolon*** in case of expression tag.
- Example:

```
<html>  
    <body>  
        Current Time: <%= java.util.Calendar.getInstance().getTime() %>  
    </body>  
</html>  
```

### (iii) Scriptlets
- A scriplet is used to execute java source code in JSP.
- It is executed at the request time and makes use of declarations, expressions and java beans.
- We can write scriptlets anywhere anywhere in a page.
- Syntax:
  `<%  java source code %>`
- Note:***Semicolon at the end of scriptlet is necessary***.
- Example
  
  `index.html`

  ```
  <html>  
    <body>  
        <form action="welcome.jsp">  
            <input type="text" name="uname">  
            <input type="submit" value="go"><br/>  
        </form>  
    </body>  
  </html>  
  ```

  `welcome.jsp`
  
  ```
  <html>  
    <body>  
    <%  
        String name=request.getParameter("uname");  
        out.print("welcome "+name);  
    %>  
    </body>  
  </html>  
  ```
## 3. Action Elements in JSP

## JSP Implicit Object
- JSP Implicit objects or predefined variables are the java objects that you can use directly without being declared first in scriptlets of JSP document. JSP implicit objects are created during the translation phase of JSP to the servlet. These variables are automatically available for the JSP page developer to use.

- There are **9 implicit objects**

| S.No | Implicit Object | Type                               | Scope      |
|------|-----------------|------------------------------------|------------|
| 1    | out             | javax.servlet.jsp.JspWriter       | Page       |
| 2    | request         | javax.servlet.HttpServletRequest   | Request    |
| 3    | response        | javax.servlet.HttpServletResponse  | Page       |
| 4    | session         | javax.servlet.http.HttpSession     | Session    |
| 5    | application     | javax.servlet.ServletContext       | Application|
| 6    | page            | javax.servlet.jsp.HttpJspPage      | Page       |
| 7    | pageContext     | javax.servlet.jsp.pageContext      | Page       |
| 8    | config          | javax.servlet.http.servletConfig   | Page       |
| 9    | exception       | java.lang.throwable                | Page       |

### 1. out
- For writing any data to the buffer, JSP provides an implicit object named out. It is the object of JspWriter.
- Example: 

```
<html>  
    <body>  
        <% out.print("Today is:"+java.util.Calendar.getInstance().getTime()); %>  
    </body>  
</html>     
```

### 2. request
- The JSP request is an implicit object of type HttpServletRequest i.e. created for each jsp request by the web container. It can be used to get request information such as parameter, header information, remote address, server name, server port, content type, character encoding etc.
- It can also be used to set, get and remove attributes from the jsp request scope.
- Example
  
  `index.html`

  ```
  <html>  
    <body>  
        <form action="welcome.jsp">  
            <input type="text" name="uname">  
            <input type="submit" value="go"><br/>  
        </form>  
    </body>  
  </html>  
  ```

  `welcome.jsp`
  
  ```
  <html>  
    <body>  
    <%  
        String name=request.getParameter("uname");  
        out.print("welcome "+name);  
    %>  
    </body>  
  </html>  
  ```
### 3. response
- In JSP, response is an implicit object of type HttpServletResponse. The instance of HttpServletResponse is created by the web container for each jsp request.
- It can be used to add or manipulate response such as redirect response to another resource, send error etc.
- Example
  
  `index.html`

  ```
  <html>  
    <body>  
        <form action="welcome.jsp">  
            <input type="text" name="uname">  
            <input type="submit" value="go"><br/>  
        </form>  
    </body>  
  </html>  
  ```

  `welcome.jsp`
  
  ```
  <%   
    response.sendRedirect("http://www.google.com");  
  %>    
  ```
### 4. session
- In JSP, session is an implicit object of type HttpSession.The Java developer can use this object to set,get or remove attribute or to get session information.
- This object is most often used when there is a need to share information between requests 
for a single user. It is used to store the user’s data to make it available on other JSP 
pages until the user session is active. This object is used to track the user information 
in the same session. 
- Example
  
  `index.html`

  ```
  <html>  
    <body>  
        <form action="welcome.jsp">  
            <input type="text" name="uname">  
            <input type="submit" value="go"><br/>  
        </form>  
    </body>  
  </html>  
  ```

  `welcome.jsp`
  
  ```
    <html>  
        <body>  
            <%   
  
                String name=request.getParameter("uname");  
                out.print("Welcome "+name);  
  
                session.setAttribute("user",name);  
  
                <a href="second.jsp">second jsp page</a>  
  
            %>  
        </body>  
    </html>    
  ```

  `second.jsp`

  ```
  <html>  
    <body>  
        <%   
  
            String name=(String)session.getAttribute("user");  
            out.print("Hello "+name);  
  
        %>  
    </body>  
  </html>  
  ```