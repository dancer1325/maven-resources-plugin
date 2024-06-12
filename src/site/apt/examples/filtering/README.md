# Goal
* Variables to include in `resources`
  * ways
    * `${...}` OR
    * `@...@`
  * can come from
    * system properties
    * project properties
    * filter resources
    * CL

## How has this project been created?
* `mvn archetype:generate -DgroupId=com.example -DartifactId=filtering -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false`
* Add the plugin skeleton indicated in the guide
  * TODO:

## How to run locally?
* `mvn resources:resources` OR `mvn resources:resources -Dname="world"`
  * based on `...resource.filtering` 
    * If it's false OR commented -> You get "Hello ${name}" in '/target/classes/hello.txt'
      * Problems:
        * Problem1: Why is NOT under 'target/extra-resources'
          * Solution: TODO:
    * If it's true -> You get "Hello ${name}" in '/target/classes/hello.txt'
      * Problems: 
        * Problem1: Same as before
        * Problem2: Why is not evaluated the expression
          * Solution: TODO:
* `mvn validate` OR `mvn validate -Dname="world"`
  * based on `...resource.filtering`
    * If it's false OR commented -> You get "Hello ${name}" in '/target/extra-resources/hello.txt'
    * If it's true -> You get "Hello filtering" OR "Hello world" in '/target/extra-resources/hello.txt'
* TODO: "Furthermore, we are not ..."

## Notes
* `mvn .... -DSomething`
  * `-D`
    * allows
      * assigning values
* Check 'maven-filtering'
* `<your.name>` property
  * evaluated because
    * Reason: 🧠 we are using 'maven-filtering' -- via -- maven-resources-plugin's filter & defined under `<properties>`🧠
* `separatedfile` property
  * specified -- by a -- separated file
  * done -- via -- `execution.configuration.filters.filter`
  * if you filter -> binary content NOT allowed!!!
    * TODO: Add example
    * Solution: Add separated folder / NO filter
