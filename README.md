# java-servlet-app

This is an example of building java servlet application using Tomcat as servlet container.

## Lessons Learned

Definition of servlet, servlet container, Apache Tomcat

- Servlet

  in application that implement Model-View-Controller (MVC) pattern, the servlet is the `Controller` that will handle the request from client and send the response back. To register the servlet you can use `@WebServlet` annotation or register it to `web.xml` file.

- Servlet Container

  this is the manager of the servlet registered to this application that will transfer request from the client to the servlet based on the requested path

- Apache Tomcat

  this is the implementation of the servlet container. We can use this application to manage and deploy our servlet application

## Run Locally

Clone the project

```bash
  git clone git@github.com:nathanaelsanilo/java-servlet-app.git
```

Go to the project directory

```bash
  cd java-servlet-app
```

Build docker image

```bash
  docker build -t app-servlet:0.1
```

Run docker container

```bash
    docker run --name app-servlet-container -d -p 8080:8080 app-servlet:0.1
```

Open browser and go to

```
http://localhost:8080/webapp/greeting
```
