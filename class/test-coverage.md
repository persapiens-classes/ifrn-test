Test Coverage
====

> [Test coverage is an important indicator in software testing in terms of quality and effectiveness. Read this blog to understand test coverage, its techniques, metrics, matrix and how to improve it.](https://www.simform.com/blog/test-coverage/) 


## Add Jacoco Plugin

Include [jacoco maven plugin](https://www.eclemma.org/jacoco/trunk/doc/maven.html) in your application pom.xml.

```xml
    <properties>
        <jacoco-maven-plugin.version>0.8.10</jacoco-maven-plugin.version>        
    </properties>

    <build>
        </pluginManagement>    
            </plugins>
                <plugin>
                    <groupId>org.jacoco</groupId>
                    <artifactId>jacoco-maven-plugin</artifactId>
                    <version>${jacoco-maven-plugin.version}</version>
                    <executions>
                        <execution>
                            <id>prepare-unit-test</id>
                            <goals>
                                <goal>prepare-agent</goal>
                            </goals>
                            <configuration>
                                <sessionId>${project.artifactId}.unit-tests</sessionId>
                            </configuration>
                        </execution>
                        <execution>
                            <id>prepare-integration-test</id>
                            <goals>
                                <goal>prepare-agent-integration</goal>
                            </goals>
                            <configuration>
                                <destFile>${project.build.directory}/jacoco.exec</destFile>
                                <append>true</append>
                                <sessionId>${project.artifactId}.integration-tests</sessionId>
                            </configuration>
                        </execution>
                        <execution>
                            <id>jacoco-report</id>
                            <goals>
                                <goal>report</goal>
                            </goals>
                        </execution>
                    </executions>
                </plugin>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-failsafe-plugin</artifactId>
                    <configuration>
                        <argLine>-Dfile.encoding=UTF-8</argLine>
                        <argLine>@{argLine} -Dfile.encoding=UTF-8</argLine>
                    </configuration>
                </plugin>                
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-surefire-plugin</artifactId>
                    <configuration>
                        <argLine>-Dfile.encoding=UTF-8</argLine>
                        <argLine>@{argLine} -Dfile.encoding=UTF-8</argLine>
                    </configuration>
                </plugin> 
            </plugins>
        </pluginManagement>    
            
        <plugins>
            <plugin>
                <groupId>org.jacoco</groupId>
                <artifactId>jacoco-maven-plugin</artifactId>
            </plugin>
        </plugins>
    </build>
```

## See Cobertura Report

Open file at target/site/jacoco/index.html

### Hands on with [Conta Example Project.](https://github.com/persapiens/conta/issues/134)

## :construction_worker: Task

Create one pull request for your project according to [Task Submission Guidelines.](../assessment.md#task-submission)

1. Add jacoco or other similar tool to create test coverage report of your application.

2. Identify missing tests of your application.

Create a **separate commit** to each subtask.
