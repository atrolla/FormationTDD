https://gitpitch.com/atrolla/FormationTDD

pom.xml :
```xml
<dependencies>
        <dependency>
            <groupId>junit</groupId>
            <artifactId>junit</artifactId>
            <version>4.12</version>
            <scope>test</scope>
        </dependency>
        <!-- https://mvnrepository.com/artifact/org.assertj/assertj-core -->
		<dependency>
			<groupId>org.assertj</groupId>
			<artifactId>assertj-core</artifactId>
			<version>3.8.0</version>
			<scope>test</scope>
		</dependency>
		<!-- if Java 7
		<dependency>
			<groupId>org.assertj</groupId>
			<artifactId>assertj-core</artifactId>
			<version>2.8.0</version>
			<scope>test</scope>
		</dependency>
		-->
    </dependencies>

    <build>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-compiler-plugin</artifactId>
                <version>3.5</version>
                <configuration>
                    <source>1.8</source>
                    <target>1.8</target>
                </configuration>
            </plugin>
        </plugins>
    </build>
```

junit 5 pom (avec java 11):
https://github.com/CodeFX-org/demo-junit-5/blob/master/pom.xml
