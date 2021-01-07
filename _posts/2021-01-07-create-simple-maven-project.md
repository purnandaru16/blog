---
layout: post
title: "Create Simple Maven Project"
date: 2021-01-07
---

1. Open **Intellij IDEA**
2. Create New Project
3. Choose **Maven** template
4. Check **Create from archetype**
5. Select **maven-archetype-webapp**
6. Next
7. Input GroupId and Artifact Name
8. Next
9. Next
10. Edit **pom.xml** and add dependencies(refresh to download dependencies)
11. Open **web.xml** and add code below
    ```sh
    <!-- Add Spring MVC DispatcherServlet as front controller -->
    <servlet>
        <servlet-name>dispatcher</servlet-name>
        <servlet-class>
            org.springframework.web.servlet.DispatcherServlet
        </servlet-class>
        <load-on-startup>1</load-on-startup>
    </servlet>

    <servlet-mapping>
        <servlet-name>dispatcher</servlet-name>
        <url-pattern>/</url-pattern>
    </servlet-mapping>
    ```
13. Create directory Java under src
14. Right click on directory, **Mark Directory As** -> **Sources Root**
15. Under Java directory, create package **com.bootcamp**
16. Under WEB-INF, create xml file with name **dispatcher-servlet.xml**
17. Add code below to dispatcher-servlet.xml
    ```sh
    <context:component-scan base-package="com.bootcamp"> </context:component-scan>

    <bean class="org.springframework.web.servlet.view.InternalResourceViewResolver">
        <property name="prefix" value="/WEB-INF/views/" />
        <property name="suffix" value=".jsp" />
    </bean>

    <!-- untuk mengaktifkan spring mvc -->
    <mvc:annotation-driven />
    ```
18. Create **HomeController.java** iside package org.bootcamp
    ```java
    package com.bootcamp;

    import org.springframework.stereotype.Controller;
    import org.springframework.ui.Model;
    import org.springframework.web.bind.annotation.GetMapping;
    import org.springframework.web.bind.annotation.RequestMapping;

    /**
     * The Class HelloController
     *
     * @author Kris Sunu Purnandaru
     */
    @RequestMapping("")
    @Controller
    public class HelloController {

        @GetMapping(value = "/homepage")
        public String home(Model model) {
            model.addAttribute("message", "Welcome!!!");

            String pesan = "Ini Homepage";
            model.addAttribute("welcome", pesan);
            return "home";
        }
    }
    ```
19. Under WEB-INF, create directory **views**
20. Add **home.jsp** inside directory **views**
    ```sh
    <%@ page contentType="text/html;charset=UTF-8" language="java" %>
    <%@ page isELIgnored="false" %>
    <html>
    <head>
        <title>Title</title>
    </head>
    <body>
    ${message}
    <br>
    ${welcome}
    </body>
    </html>
    ```
