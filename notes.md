# Additional build notes

Was running into errors when using the build notes in the readme.md

```sh
salim@dev:~/Dev/rdap_bootstrap_server$ ./gradlew clean build test

FAILURE: Build failed with an exception.

* Where:
Settings file '/home/salim/Dev/rdap_bootstrap_server/settings.gradle'

* What went wrong:
Could not compile settings file '/home/salim/Dev/rdap_bootstrap_server/settings.gradle'.
> startup failed:
  General error during semantic analysis: Unsupported class file major version 61
  
  java.lang.IllegalArgumentException: Unsupported class file major version 61
        at groovyjarjarasm.asm.ClassReader.<init>(ClassReader.java:196)
        at groovyjarjarasm.asm.ClassReader.<init>(ClassReader.java:177)
        at groovyjarjarasm.asm.ClassReader.<init>(ClassReader.java:163)
        at groovyjarjarasm.asm.ClassReader.<init>(ClassReader.java:284)
```

Made changes to gradle/wrapper/gradle-wrapper.properties to use gradle-7.0-bin.zip. 

Following are the specs of the dev machine:

* Linux f127 5.11.0-37-generic #41~20.04.2-Ubuntu SMP Fri Sep 24 09:06:38 UTC 2021 x86_64 x86_64 x86_64 GNU/Linux
* Ubuntu 20.04.3 LTS
* OpenJDK 11 (java-11-openjdk-amd64)

Build command:

```sh
./gradlew clean build test
```
