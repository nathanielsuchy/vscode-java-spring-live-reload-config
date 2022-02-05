# vscode-java-spring-live-reload-config
This is the configuration I've found works best to support Java and Spring Boot with Live Reload of Templates and Static Assets without an Application Server restart

## How to use this

1. Create a Spring Boot Project at https://start.spring.io/
2. Download this repo and copy the contents into your project (you might want to skip LICENSE and README.md)
3. Edit `launch.json` and replace the main class name from `com.company.Main.ApplicationServer` to the correct fully qualified class path on line 11 and 27.