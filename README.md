# Gradle script plugins

## Usage

Add to the Root `build.gradle`

```
apply from: "https://raw.githubusercontent.com/anaxo-io/gradle-plugins/master/root/buildscript.gradle"
apply from: "https://raw.githubusercontent.com/anaxo-io/gradle-plugins/master/root/gradle-wrapper.gradle"
apply from: "https://raw.githubusercontent.com/anaxo-io/gradle-plugins/master/root/profiles-config.gradle"
apply from: "https://raw.githubusercontent.com/anaxo-io/gradle-plugins/master/root/deployment.gradle"
apply from: "https://raw.githubusercontent.com/anaxo-io/gradle-plugins/master/root/test-reports.gradle"
```

Add to Java subproject build.gradle
```
apply from: "https://raw.githubusercontent.com/anaxo-io/gradle-plugins/master/java/java-plugins.gradle"
apply from: "https://raw.githubusercontent.com/anaxo-io/gradle-plugins/master/java/dependencies.gradle"
apply from: "https://raw.githubusercontent.com/anaxo-io/gradle-plugins/master/java/integration-test.gradle"
apply from: "https://raw.githubusercontent.com/anaxo-io/gradle-plugins/master/java/sonarqube.gradle"
```

Add to Docker subproject build.gradle
```
project.ext.imageSource = project("<Java_Project>").name
project.ext.imageName = "${name}:${version}"
project.ext.imagePort = <Exposed_Port>

apply from: "https://raw.githubusercontent.com/anaxo-io/gradle-plugins/master/devops/docker.gradle"
```