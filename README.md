**##Vulnerable as Hell**

## How to run the demo (Maven)
1. Checkout this repository (`git checkout git@github.com:snyk/java-reachability-playground.git`)
2. Install all the dependencies (`mvn install`)
3. Compile the project (`mvn compile`)
4. Run the main class (`mvn exec:java -Dexec.mainClass=Unzipper`); the application should throw an exception saying `Malicious file /tmp/evil.txt was created`.
5. Run snyk command with Reachable Vulnerabilities flag (`snyk test --reachable` or `snyk monitor --reachable`); you should see the vulnerability `SNYK-JAVA-ORGND4J-72550` marked as reachable
and the function call path to the vulnerability

## For Gradle 
1. Make sure you build the artifacts with `./gradlew build`
2. To see test results run `snyk test --file=build.gradle --reachable` or monitor: `snyk monitor --file=build.gradle --reachable`
---

