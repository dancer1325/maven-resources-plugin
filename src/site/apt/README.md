* allows
  * project resources -- are copied to -- output directory
    * project resources can be filtered -- via -- [Maven Filtering](https://maven.apache.org/shared/maven-filtering/)
* type of resources
  * main resources
    * := resources / -- associated to -- main source code
  * test resources
    * := resources / -- associated to -- test source code
* goals == ways to specify resource & output directory elements 
  * `resources:resources`
    * main resources -- are copied to -- main output directory
      * test resources NOT copied!!!
    * executed automatically
      * Reason: 🧠 bounded by default to 'process-resources' life-cycle phase -- [Link](https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html#setting-up-your-project-to-use-the-build-lifecycle) -- 🧠
    * elements
      * 'project.build.resources'
        * -- allows specifying the -- main resources
      * 'project.build.outputDirectory'
        * -- allows specifying the -- main output directory
  * `resources:testResources`
    * test resources -- are copied to -- test output directory
      * main resources NOT copied!!!
    * executed automatically
      * Reason: 🧠 bounded by default to 'process-test-resources' life-cycle phase -- [Link](https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html#setting-up-your-project-to-use-the-build-lifecycle) -- 🧠
    * elements
      * 'project.build.testResources'
        * -- allows specifying the -- test resources
      * 'project.build.testOutputDirectory'
        * -- allows specifying the -- test output directory
  * `resources:copy-resources`
    * resources -- are copied to -- output directory
      * TODO: Which resources are referred here?

## Examples
* Check 
  * 'usage/'
  * 'examples/'