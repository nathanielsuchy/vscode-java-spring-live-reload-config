# vscode-java-spring-live-reload-config
This is the configuration I've found works best to support Java and Spring Boot with Live Reload of Templates and Static Assets without an Application Server restart.

## What does this configure

This configures a VS Code Remote Containers Environment to run Java 11 with MariaDB in another container. Additionally it configures Spring Boot to use a different `application.properties` file called `application-dev.properties` which is passed in as a `vmArgs` argument. This tells Spring Boot to not cache templates or static assets in development mode. Normally they are copied to and loaded from `target/**`. This allows you to update the templates and static updates without restarting the application server to test your changes. On one project I've found this saves approtimately 14 seconds per tested change. For larger applications the benefits are likely greater.

## How to use this config

1. Create a Spring Boot Project at https://start.spring.io/ with Spring Data JPA, Thymeleaf, Developer Tools, and the MariaDB Driver and anything else you might need.
2. Download this repo and copy the contents into your project (you might want to skip LICENSE and README.md)
3. Edit `launch.json` and replace the main class name from `com.company.Main.ApplicationServer` to the correct fully qualified class path on lines 11 and 27.