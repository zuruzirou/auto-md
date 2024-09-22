# File Tree

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


---

# pom

## Metadata
- **Generated on:** 2024-09-22 15:11:19
- **Source:** maven_common

# pom

<?xml version="1.0" encoding="UTF-8"?> <project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd"> <modelVersion>4.0.0</modelVersion> <parent> <groupId>org.springframework.boot</groupId> <artifactId>spring-boot-starter-parent</artifactId> <version>3.1.2</version> <relativePath/> <!-- lookup parent from repository --> </parent> <groupId>com.example</groupId> <artifactId>maven_common</artifactId> <version>${build_time}</version> <name>maven_common</name> <description>Demo project for Spring Boot</description> <properties> <java.version>17</java.version> </properties> <dependencies> <dependency> <groupId>org.springframework.boot</groupId> <artifactId>spring-boot-starter</artifactId> </dependency> <dependency> <groupId>org.springframework.boot</groupId> <artifactId>spring-boot-starter-test</artifactId> <scope>test</scope> </dependency> </dependencies> <distributionManagement> <repository> <id>github</id> <name>GitHub Packages</name> <url>https://maven.pkg.github.com/coding-sample/maven_common/releases</url> </repository> <snapshotRepository> <id>github</id> <name>GitHub Packages</name> <url>https://maven.pkg.github.com/coding-sample/maven_common/snapshots</url> </snapshotRepository> </distributionManagement> <build> <plugins> <!-- spring-boot-maven-plugin --> </plugins> </build> </project>


---

# README

## Metadata
- **Generated on:** 2024-09-22 15:11:19
- **Source:** maven_common

# README

#  ## Workflow permissions Read and write permissions ## Access Accessible from repositories in the 'coding-sample' organization # template 1. Webtemplate 1. pom.xmlmaven_common3 1. organizationdistributionManagement https://maven.pkg.github.com/zuruorg3/comm1 1. settings 1. Actions -> General -> Read and write permissions 1. Actions -> General -> Accessible from repositories owned by the user 'zuruzirou' 1. actionsNG # template 1. VSCSpring Initializer 1. setting.xmlpom.xmldistributionManagementworkflow file 1. packages 1. web 1. Actions -> General -> Read and write permissions 1. Actions -> General -> Accessible from repositories owned by the user 'zuruzirou' 1. settingstemplate project # using: "composite"  https://docs.github.com/ja/actions/creating-actions/creating-a-composite-action # repository_dispatch https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#repository_dispatch PKG_READ_ETERNAL # tag git push --delete origin hoge10 git tag -d hoge10 git tag hoge10 git push origin hoge10 https://docs.github.com/ja/rest/actions/workflows?apiVersion=2022-11-28#create-a-workflow-dispatch-event


---

# settings

## Metadata
- **Generated on:** 2024-09-22 15:11:19
- **Source:** maven_common

# settings

<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 https://maven.apache.org/xsd/settings-1.0.0.xsd"> <servers> <server> <id>github</id> <username>${env.GITHUB_ACTOR}</username> <password>${env.GITHUB_TOKEN}</password> </server> </servers> </settings>


---

# StringUtil

## Metadata
- **Generated on:** 2024-09-22 15:11:19
- **Source:** maven_common

# StringUtil

package com.example.maven_common; public class StringUtil { public String getRepo() { return "Comm"; } }


---

# StringUtilTest

## Metadata
- **Generated on:** 2024-09-22 15:11:19
- **Source:** maven_common

# StringUtilTest

package com.example.maven_common; import static org.junit.jupiter.api.Assertions.assertEquals; import org.junit.jupiter.api.Test; public class StringUtilTest { @Test public void test() { StringUtil comm = new StringUtil(); assertEquals("Comm", comm.getRepo()); } }

