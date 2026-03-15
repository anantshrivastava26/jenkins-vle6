# Jenkins CI Pipeline with Maven

## Project Overview

This project demonstrates **Continuous Integration (CI)** using **Jenkins and Maven**.
Whenever code is pushed to the GitHub repository, Jenkins automatically pulls the code, builds the Java application using Maven, and generates a build artifact.

The project contains a simple Java program that prints a message when executed.

---

## Objective

To implement a **Continuous Integration pipeline** where:

* Source code is stored in **GitHub**
* **Jenkins** monitors the repository
* **Maven** compiles the Java application
* Jenkins displays the **build status**

---

## Technology Stack

| Component            | Tool            |
| -------------------- | --------------- |
| Version Control      | Git             |
| Repository           | GitHub          |
| CI/CD Tool           | Jenkins         |
| Build Tool           | Maven           |
| Programming Language | Java            |
| Operating System     | Windows / Linux |

---

## Project Structure

```
jenkins-vle6
│
├── src
│   └── HelloWorld.java
│
├── pom.xml
│
└── README.md
```

---

## Java Program

```
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello from Jenkins CI Pipeline!");
    }
}
```

---

## Maven Configuration (pom.xml)

The project uses Maven to compile the Java source code.

```
<build>
  <sourceDirectory>src</sourceDirectory>

  <plugins>
    <plugin>
      <artifactId>maven-compiler-plugin</artifactId>
      <version>3.8.1</version>

      <configuration>
        <source>17</source>
        <target>17</target>
      </configuration>

    </plugin>
  </plugins>
</build>
```

---

## Jenkins CI Workflow

```
Developer
   ↓
Push Code to GitHub
   ↓
Jenkins detects change
   ↓
Jenkins pulls repository
   ↓
Maven compiles Java project
   ↓
JAR artifact generated
```

---

## Jenkins Job Configuration

### Source Code Management

```
Repository URL:
https://github.com/anantshrivastava26/jenkins-vle6
Branch:
*/main
```

### Build Step

```
Invoke top-level Maven targets
Goals:
clean package
```

---

## Build Output

When Jenkins runs the build, Maven generates the compiled artifact:

```
target/jenkins-lab-1.0.jar
```

Console Output:

```
[INFO] BUILD SUCCESS
```

---

## How to Run the Project Manually

Clone the repository:

```
git clone https://github.com/anantshrivastava26/jenkins-vle6.git
cd jenkins-vle6
```

Build using Maven:

```
mvn clean package
```

Run the compiled program:

```
java -cp target/jenkins-lab-1.0.jar HelloWorld
```

---

## Result

The Continuous Integration pipeline was successfully implemented using **Jenkins and Maven**, where Jenkins automatically builds the Java application and generates a build artifact whenever the code is updated.

---

## Author

Anant Shrivastava
