---
layout: post
title: "Create Simple Maven Project"
date: 2021-01-07
---

1. Open Intellij IDEA
2. Create New Project
3. Choose Maven template
4. Check Create from archetype
5. Select maven-archetype-webapp
6. Next
7. Input GroupId and Artifact Name
8. Next
9. Next
10. Edit pom.xml and add dependencies(refresh to download dependencies)
11. Open web.xml
12. Add servlet
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
14. Right click on directory, Mark Directory As Sources Root

