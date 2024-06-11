# Goal
* Specify files rather than WHOLE directories (== ALL files | directory)
  * `resources.resource.includes.include`
    * if you specify it -> REST of files NOT included
  * `resources.resource.excludes.exclude`

## How has this project been created?
* `mvn archetype:generate -DgroupId=com.example -DartifactId=include-exclude-files-and-directories -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false`
* Add the plugin skeleton indicated in the guide

## How to run locally?
* `mvn clean package`
  * ALSO contains 'validate' phase -> Check the files copied under 'target/extra-resources'
    * excluded
      * 'src/my-resources/alfredtest.txt'
      * 'src/my-resources/config.properties'
        * Reason: 🧠If you specify included -> rest excluded automatically  🧠
      * 'src/my-resources/nomad.jpg'
        * Reason: 🧠excluded specifically 🧠
    * included
      * 'alfred.txt'
* `mvn validate`
  * Check the previous command checkers
* `mvn resources:resources`
  * Problems
    * Problem1: Why has NOTHING being copied?
      * Solution: TODO:

## Notes
* `resource.directory`
  * include ALL the resources | directory
