![jenkins success build](https://github.com/user-attachments/assets/ed76a8d0-27ed-4e91-afc6-cf862803c08f)



[✅ Summary: Complete Jenkins + Maven Java Build on EC2]


Step	Action	Purpose
1	Launch EC2 Instance (Amazon Linux 2)	Create a cloud server for Jenkins setup
2	Connect to EC2 via PuTTY	Access and control your EC2 instance
3	Install Java (Amazon Corretto 8)	Required for compiling and running Java code
4	Install Apache Maven	Build tool to compile and package Java apps
5	Install Jenkins	The CI/CD automation server
6	Start Jenkins Service	Enable Jenkins and ensure it's running
7	Access Jenkins via Browser	Visit Jenkins web UI on http://52.38.179.74:8080
8	Unlock Jenkins and Install Plugins	Initial setup of Jenkins after installation
9	Create HelloWorld Java App + pom.xml	Basic Java Maven project for testing
10	Push Project to GitHub	So Jenkins can pull the project and build it
11	Create Jenkins Freestyle Project	Configure job to build Java app using Maven
12	Build the Jenkins Job	Trigger a build and verify BUILD SUCCESS
13	Capture Screenshot & Push to GitHub	Evidence of success; submit your repo link

 src/main/java/HelloWorld.java

public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, Jenkins + Maven!");
    }
}


[ pom.xml ]

<project>
  <modelVersion>4.0.0</modelVersion>
  <groupId>com.example</groupId>
  <artifactId>hello</artifactId>
  <version>1.0</version>
  <build>
    <plugins>
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-compiler-plugin</artifactId>
        <version>3.8.1</version>
        <configuration>
          <source>1.8</source>
          <target>1.8</target>
        </configuration>
      </plugin>
    </plugins>
  </build>
</project>



[Final GitHub Repository Structure]

hello-java-maven/
├── pom.xml
├── jenkins-build-success.png
└── src/
    └── main/
        └── java/
            └── HelloWorld.java
