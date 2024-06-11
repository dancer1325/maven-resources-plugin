# Goal
* Use the goal 'resources:copy-resources' /
  * copy resources / NOT placed neither
    * default maven layout nor
    * 'build/resources'
* Check 'copy-resources/'

## How has this project been created?
* `mvn archetype:generate -DgroupId=com.example -DartifactId=copy-resources -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false`
* Add resources under 'src/non-packaged-resources'
* Add the plugin skeleton indicated in the guide

## How to run locally?
* `mvn clean package`
  * ALSO contains 'validate' phase -> Check the files copied under 'target/extra-resources'
* `mvn validate`
  * Check the files copied under 'target/extra-resources'
* `mvn resources:copy-resources`
  * Problems:
    * Problem1: "The parameters 'resources', 'outputDirectory' for goal org.apache.maven.plugins:maven-resources-plugin:3.3.1:copy-resources are missing or invalid"
      * Solution: TODO:
