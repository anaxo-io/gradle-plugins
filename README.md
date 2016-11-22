# Gradle script plugins

## Usage

Add to the root `build.gradle`

```
buildscript {
    apply from: 'https://raw.githubusercontent.com/anaxo-io/gradle-plugins/master/buildscript.gradle', to: buildscript
}
apply from: 'https://raw.githubusercontent.com/anaxo-io/gradle-plugins/master/root/gradle-wrapper.gradle"
apply from: 'https://raw.githubusercontent.com/anaxo-io/gradle-plugins/master/root/profiles-config.gradle"
apply from: 'https://raw.githubusercontent.com/anaxo-io/gradle-plugins/master/root/test-reports.gradle"
```

Add to the subprojects build.gradle
```
apply from: 'https://raw.githubusercontent.com/anaxo-io/gradle-plugins/master/projects/java-plugins.gradle"
apply from: 'https://raw.githubusercontent.com/anaxo-io/gradle-plugins/master/projects/dependencies.gradle"
apply from: 'https://raw.githubusercontent.com/anaxo-io/gradle-plugins/master/projects/integration-test.gradle"
apply from: 'https://raw.githubusercontent.com/anaxo-io/gradle-plugins/master/projects/deployment.gradle"
apply from: 'https://raw.githubusercontent.com/anaxo-io/gradle-plugins/master/projects/sonarqube.gradle"
```