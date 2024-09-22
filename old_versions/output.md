# File Tree

- maven_common
  - pom.xml
  - README.md
  - settings.xml
  - src
    - main
      - java
        - com
          - example
            - maven_common
              - StringUtil.java
    - test
      - java
        - com
          - example
            - maven_common
              - StringUtilTest.java
- maven_logic
  - pom.xml
  - README.md
  - settings.xml
  - src
    - main
      - java
        - com
          - example
            - maven_logic
              - Logic.java
    - test
      - java
        - com
          - example
            - maven_logic
              - LogicTest.java
- maven_web
  - pom.xml
  - README.md
  - settings.xml
  - src
    - main
      - java
        - com
          - example
            - maven_web
              - Application.java
              - controller
                - ApiController.java
    - test
      - java
        - com
          - example
            - maven_logic
              - ApplicationTests.java


---

# pom

## Metadata
- **Generated on:** 2024-09-22 15:41:58
- **Source:** maven_common

# pom

<?xml version="1.0" encoding="UTF-8"?> <project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd"> <modelVersion>4.0.0</modelVersion> <parent> <groupId>org.springframework.boot</groupId> <artifactId>spring-boot-starter-parent</artifactId> <version>3.1.2</version> <relativePath/> <!-- lookup parent from repository --> </parent> <groupId>com.example</groupId> <artifactId>maven_common</artifactId> <version>${build_time}</version> <name>maven_common</name> <description>Demo project for Spring Boot</description> <properties> <java.version>17</java.version> </properties> <dependencies> <dependency> <groupId>org.springframework.boot</groupId> <artifactId>spring-boot-starter</artifactId> </dependency> <dependency> <groupId>org.springframework.boot</groupId> <artifactId>spring-boot-starter-test</artifactId> <scope>test</scope> </dependency> </dependencies> <distributionManagement> <repository> <id>github</id> <name>GitHub Packages</name> <url>https://maven.pkg.github.com/coding-sample/maven_common/releases</url> </repository> <snapshotRepository> <id>github</id> <name>GitHub Packages</name> <url>https://maven.pkg.github.com/coding-sample/maven_common/snapshots</url> </snapshotRepository> </distributionManagement> <build> <plugins> <!-- spring-boot-maven-plugin --> </plugins> </build> </project>


---

# README

## Metadata
- **Generated on:** 2024-09-22 15:41:58
- **Source:** maven_common

# README

#  ## Workflow permissions Read and write permissions ## Access Accessible from repositories in the 'coding-sample' organization # template 1. Webtemplate 1. pom.xmlmaven_common3 1. organizationdistributionManagement https://maven.pkg.github.com/zuruorg3/comm1 1. settings 1. Actions -> General -> Read and write permissions 1. Actions -> General -> Accessible from repositories owned by the user 'zuruzirou' 1. actionsNG # template 1. VSCSpring Initializer 1. setting.xmlpom.xmldistributionManagementworkflow file 1. packages 1. web 1. Actions -> General -> Read and write permissions 1. Actions -> General -> Accessible from repositories owned by the user 'zuruzirou' 1. settingstemplate project # using: "composite"  https://docs.github.com/ja/actions/creating-actions/creating-a-composite-action # repository_dispatch https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#repository_dispatch PKG_READ_ETERNAL # tag git push --delete origin hoge10 git tag -d hoge10 git tag hoge10 git push origin hoge10 https://docs.github.com/ja/rest/actions/workflows?apiVersion=2022-11-28#create-a-workflow-dispatch-event


---

# settings

## Metadata
- **Generated on:** 2024-09-22 15:41:58
- **Source:** maven_common

# settings

<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 https://maven.apache.org/xsd/settings-1.0.0.xsd"> <servers> <server> <id>github</id> <username>${env.GITHUB_ACTOR}</username> <password>${env.GITHUB_TOKEN}</password> </server> </servers> </settings>


---

# StringUtil

## Metadata
- **Generated on:** 2024-09-22 15:41:58
- **Source:** maven_common

# StringUtil

package com.example.maven_common; public class StringUtil { public String getRepo() { return "Comm"; } }


---

# StringUtilTest

## Metadata
- **Generated on:** 2024-09-22 15:41:58
- **Source:** maven_common

# StringUtilTest

package com.example.maven_common; import static org.junit.jupiter.api.Assertions.assertEquals; import org.junit.jupiter.api.Test; public class StringUtilTest { @Test public void test() { StringUtil comm = new StringUtil(); assertEquals("Comm", comm.getRepo()); } }


---

# pom

## Metadata
- **Generated on:** 2024-09-22 15:41:59
- **Source:** maven_logic

# pom

<?xml version="1.0" encoding="UTF-8"?> <project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd"> <modelVersion>4.0.0</modelVersion> <parent> <groupId>org.springframework.boot</groupId> <artifactId>spring-boot-starter-parent</artifactId> <version>3.1.2</version> <relativePath/> <!-- lookup parent from repository --> </parent> <groupId>com.example</groupId> <artifactId>maven_logic</artifactId> <version>${build_time}</version> <name>maven_logic</name> <description>Demo project for Spring Boot</description> <properties> <java.version>17</java.version> </properties> <repositories> <repository> <id>github_releases</id> <name>GitHub Packages releases</name> <url>https://maven.pkg.github.com/coding-sample/maven_common/releases</url> </repository> <repository> <id>github_snapshots</id> <name>GitHub Packages snapshots</name> <url>https://maven.pkg.github.com/coding-sample/maven_common/snapshots</url> <snapshots> <enabled>true</enabled> </snapshots> </repository> </repositories> <distributionManagement> <repository> <id>github</id> <name>GitHub Packages</name> <url>https://maven.pkg.github.com/coding-sample/maven_logic/releases</url> </repository> <snapshotRepository> <id>github</id> <name>GitHub Packages</name> <url>https://maven.pkg.github.com/coding-sample/maven_logic/snapshots</url> </snapshotRepository> </distributionManagement> <dependencies> <dependency> <groupId>com.example</groupId> <artifactId>maven_common</artifactId> <version>${build_time}</version> </dependency> <dependency> <groupId>org.springframework.boot</groupId> <artifactId>spring-boot-starter</artifactId> </dependency> <dependency> <groupId>org.springframework.boot</groupId> <artifactId>spring-boot-starter-test</artifactId> <scope>test</scope> </dependency> </dependencies> <build> <plugins> </plugins> </build> </project>


---

# README

## Metadata
- **Generated on:** 2024-09-22 15:41:59
- **Source:** maven_logic

# README

# template 1. Webtemplate 1. pom.xmlmaven_logic2 1. pom.xmlmaven_common2 1. settings 1. Personal Access Tokenread:packagesOK 1. actionsNG # template 1. VSCSpring Initializer 1. setting.xmlpom.xmlrepositoryworkflow file 1. commonpackages 1. web 1. Personal Access Tokenread:packagesOK 1. PAT # Github Apps 1. organization 1. settings-> Developper settings -> Gihtub Apps -> New Github App 1. URL 1. WebhookActiveOFF 1. Repository PermissionPakcagesread-onlyMetadata 1.  1. Private keys 1. pemDL # Github Apps 1. organizationsettings -> Github Apps -> App 1. Install App -> organization 1. settings -> secrets and variables -> Secrets 1. APP_ID=378486 workflow 1. PRIVATE_KEY=pem workflow


---

# settings

## Metadata
- **Generated on:** 2024-09-22 15:41:59
- **Source:** maven_logic

# settings

<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 https://maven.apache.org/xsd/settings-1.0.0.xsd"> <servers> <server> <id>github</id> <username>${env.GITHUB_ACTOR}</username> <password>${env.GITHUB_TOKEN}</password> </server> <server> <id>github_releases</id> <username>${env.GITHUB_ACTOR}</username> <password>${env.GITHUB_TOKEN}</password> </server> <server> <id>github_snapshots</id> <username>${env.GITHUB_ACTOR}</username> <password>${env.GITHUB_TOKEN}</password> </server> </servers> </settings>


---

# Logic

## Metadata
- **Generated on:** 2024-09-22 15:41:59
- **Source:** maven_logic

# Logic

package com.example.maven_logic; import com.example.maven_common.StringUtil; public class Logic { private StringUtil stringUtil; public Logic() { this.stringUtil = new StringUtil(); } public String processData(String input) { if (input == null || input.isEmpty()) { return "No input provided"; } StringBuilder result = new StringBuilder(); for (int i = 0; i < input.length(); i++) { char c = input.charAt(i); if (Character.isLetter(c)) { result.append(Character.toUpperCase(c)); } else if (Character.isDigit(c)) { result.append((char)(c + 1)); } else { result.append(c); } } // Use StringUtil's method result.append(" - ").append(stringUtil.getRepo()); return result.toString(); } public int calculateSum(int[] numbers) { int sum = 0; for (int num : numbers) { sum += num; } return sum; } }


---

# LogicTest

## Metadata
- **Generated on:** 2024-09-22 15:41:59
- **Source:** maven_logic

# LogicTest

package com.example.maven_logic; import org.junit.jupiter.api.Test; import static org.junit.jupiter.api.Assertions.*; public class LogicTest { @Test public void testProcessData_WithNullInput() { Logic logic = new Logic(); String result = logic.processData(null); assertEquals("No input provided", result); } @Test public void testProcessData_WithValidInput() { Logic logic = new Logic(); String result = logic.processData("abc123!"); assertEquals("ABC234! - Comm", result); // Updated expected result } @Test public void testCalculateSum() { Logic logic = new Logic(); int[] numbers = {1, 2, 3, 4, 5}; int sum = logic.calculateSum(numbers); assertEquals(15, sum); } }


---

# pom

## Metadata
- **Generated on:** 2024-09-22 15:42:00
- **Source:** maven_web

# pom

<?xml version="1.0" encoding="UTF-8"?> <project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd"> <modelVersion>4.0.0</modelVersion> <parent> <groupId>org.springframework.boot</groupId> <artifactId>spring-boot-starter-parent</artifactId> <version>3.1.2</version> <relativePath/> <!-- lookup parent from repository --> </parent> <groupId>com.example</groupId> <artifactId>maven_web</artifactId> <!--  --> <version>${build_time}</version> <name>maven_web</name> <!--  --> <description>Demo project for Spring Boot</description> <properties> <java.version>17</java.version> </properties> <repositories> <repository> <id>github_releases</id> <name>GitHub Packages releases</name> <url>https://maven.pkg.github.com/coding-sample/maven_common/releases</url> </repository> <repository> <id>github_snapshots</id> <name>GitHub Packages snapshots</name> <url>https://maven.pkg.github.com/coding-sample/maven_common/snapshots</url> <snapshots> <enabled>true</enabled> </snapshots> </repository> </repositories> <distributionManagement> <repository> <id>github</id> <name>GitHub Packages</name> <url>https://maven.pkg.github.com/coding-sample/maven_web/releases</url> <!--  --> </repository> <snapshotRepository> <id>github</id> <name>GitHub Packages</name> <url>https://maven.pkg.github.com/coding-sample/maven_web/snapshots</url> <!--  --> </snapshotRepository> </distributionManagement> <dependencies> <dependency> <groupId>com.example</groupId> <artifactId>maven_common</artifactId> <version>${build_time}</version> </dependency> <dependency> <groupId>org.springframework.boot</groupId> <artifactId>spring-boot-starter</artifactId> </dependency> <dependency> <groupId>org.springframework.boot</groupId> <artifactId>spring-boot-starter-test</artifactId> <scope>test</scope> </dependency> <dependency> <groupId>junit</groupId> <artifactId>junit</artifactId> <version>4.13.2</version> <scope>test</scope> </dependency> <dependency> <groupId>org.springframework.boot</groupId> <artifactId>spring-boot-starter-web</artifactId> </dependency> <dependency> <groupId>com.example</groupId> <artifactId>maven_logic</artifactId> <version>${build_time}</version> </dependency> </dependencies> <build> <plugins> <plugin> <groupId>org.springframework.boot</groupId> <artifactId>spring-boot-maven-plugin</artifactId> </plugin> </plugins> </build> </project>


---

# README

## Metadata
- **Generated on:** 2024-09-22 15:42:00
- **Source:** maven_web

# README

# template 1. Webtemplate 1. pom.xmlmaven_web2 1. pom.xmlmaven_common2 1. settings 1. Personal Access Tokenread:packagesOK 1. actionsNG # template 1. VSCSpring Initializer 1. setting.xmlpom.xmlrepositoryworkflow file 1. commonpackages 1. web 1. Personal Access Tokenread:packagesOK 1. PAT # Github Apps 1. organization 1. settings-> Developper settings -> Gihtub Apps -> New Github App 1. URL 1. WebhookActiveOFF 1. Repository PermissionPakcagesread-onlyMetadata 1.  1. Private keys 1. pemDL # Github Apps 1. organizationsettings -> Github Apps -> App 1. Install App -> organization 1. settings -> secrets and variables -> Secrets 1. APP_ID=378486 workflow 1. PRIVATE_KEY=pem workflow # API - `GET /api/hello`: "Hello, World!"


---

# settings

## Metadata
- **Generated on:** 2024-09-22 15:42:00
- **Source:** maven_web

# settings

<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 https://maven.apache.org/xsd/settings-1.0.0.xsd"> <servers> <server> <id>github</id> <username>${env.GITHUB_ACTOR}</username> <password>${env.GITHUB_TOKEN}</password> </server> <server> <id>github_releases</id> <username>${env.GITHUB_ACTOR}</username> <password>${env.GITHUB_TOKEN}</password> </server> <server> <id>github_snapshots</id> <username>${env.GITHUB_ACTOR}</username> <password>${env.GITHUB_TOKEN}</password> </server> </servers> </settings>


---

# Application

## Metadata
- **Generated on:** 2024-09-22 15:42:00
- **Source:** maven_web

# Application

package com.example.maven_web; import org.springframework.boot.SpringApplication; import org.springframework.boot.autoconfigure.SpringBootApplication; @SpringBootApplication public class Application { public static void main(String[] args) { SpringApplication.run(Application.class, args); } }


---

# ApiController

## Metadata
- **Generated on:** 2024-09-22 15:42:00
- **Source:** controller

# ApiController

package com.example.maven_web.controller; import com.example.maven_logic.Logic; //  import org.springframework.beans.factory.annotation.Autowired; import org.springframework.web.bind.annotation.GetMapping; import org.springframework.web.bind.annotation.RequestMapping; import org.springframework.web.bind.annotation.RestController; @RestController @RequestMapping("/api") public class ApiController { @Autowired private Logic logic; //  @GetMapping("/hello") public String sayHello() { return "Hello, World!"; } @GetMapping("/api/hello") public String hello() { //  String message = "Hello, World!"; // maven_logic String logicResult = logic.processData("sample input"); //  return message + " " + logicResult; } }


---

# ApplicationTests

## Metadata
- **Generated on:** 2024-09-22 15:42:00
- **Source:** maven_logic

# ApplicationTests

package com.example.maven_logic; import org.junit.Test; import org.junit.runner.RunWith; import org.springframework.test.context.junit4.SpringRunner; @RunWith(SpringRunner.class) public class ApplicationTests { @Test public void contextLoads() { //  } }

