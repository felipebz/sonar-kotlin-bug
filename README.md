Steps to reproduce:

- Start a SonarQube 8.6 instance.
- Run `./mvnw verify sonar:sonar`.

The SonarQube analysis will cause the exception below:

`
[ERROR] Failed to execute goal org.sonarsource.scanner.maven:sonar-maven-plugin:3.7.0.1746:sonar (default-cli) on project sonar-kotlin-bug: Can not add the same measure twice on module1/src/test/kotlin/org/example/HelloTest.kt: DefaultMeasure[component=module1/src/test/kotlin/org/example/HelloTest.kt,metric=Metric[uuid=<null>,key=skipped_tests,description=Number of skipped unit tests,type=INT,direction=-1,domain=Coverage,name=Skipped Unit Tests,qualitative=true,userManaged=false,enabled=true,worstValue=<null>,bestValue=0.0,optimizedBestValue=true,hidden=false,deleteHistoricalData=false,decimalScale=<null>],value=0,fromCore=false,storage=org.sonar.scanner.sensor.DefaultSensorStorage@2d6aefe1,saved=false] -> [Help 1]
`
