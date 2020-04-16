# README

This is a maven project that will allow the build, unit tests, and integration tests to run in parallel.

## Parallel Build

By utilizing maven [projcect specific command line options][projcect-specific-jvm-and-command-line-options], all modules run with the option of 1T.  This gives the build 1 thread per core on the machine and allows multiple modules to build in parallel.  For more information see the [maven parallel builds documentation][maven-parallel-builds].

## Parallel Unit Tests

The maven surefire plugin supports running unit test in parallel by suite, classes, or methods.  This configuration runs each individual method (unit test) in parallel with 1 thread per core witha maximum of 16 threads.  For more information see the [maven surfire plugin documentation on fork options and parallel test execution][surefire-documentation].

## Parallel Integration Tests

The maven failsafe plugin supports running unit test in parallel by suite, classes, or methods.  This configuration runs each individual method (integration test) in parallel with 1 thread per core witha maximum of 16 threads.  For more information see the [maven failsafe plugin documentation on fork options and parallel test execution][failsafe-documentation].

   [projcect-specific-jvm-and-command-line-options]: <https://maven.apache.org/docs/3.3.1/release-notes.html#JVM_and_Command_Line_Options>
   [maven-jira-ticket]: <https://issues.apache.org/jira/browse/MNG-5767>
   [maven-parallel-builds]: <https://cwiki.apache.org/confluence/display/MAVEN/Parallel+builds+in+Maven+3>
   
   [surefire-documentation]:<https://maven.apache.org/surefire/maven-surefire-plugin/examples/fork-options-and-parallel-execution.html>

   [failsafe-documentation]:<https://maven.apache.org/surefire/maven-failsafe-plugin/examples/fork-options-and-parallel-execution.html>

