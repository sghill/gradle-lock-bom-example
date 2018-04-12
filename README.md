Gradle Lock Bom Example
=======================

Lock files generated with `./gradlew dependencies --write-locks`

Branch: master
--------------

* Uses [nebula.dependency-recommender](https://plugins.gradle.org/plugin/nebula.dependency-recommender)
* `./gradlew build` fails with transitives that are present in the lock

```
FAILURE: Build failed with an exception.

* What went wrong:
Could not resolve all dependencies for configuration ':compileClasspath'.
> Dependency lock state for configuration 'compileClasspath' is out of date::
    - Resolved 'org.springframework:spring-aop:5.0.5.RELEASE' which is not part of the lock state
    - Resolved 'org.springframework:spring-beans:5.0.5.RELEASE' which is not part of the lock state
    - Resolved 'org.springframework:spring-core:5.0.5.RELEASE' which is not part of the lock state
    - Resolved 'org.springframework:spring-expression:5.0.5.RELEASE' which is not part of the lock state
    - Resolved 'org.springframework:spring-jcl:5.0.5.RELEASE' which is not part of the lock state
```

Branch: new-bom-support
-----------------------

* Uses `enableFeaturePreview('IMPROVED_POM_SUPPORT')` in settings.gradle
* `./gradlew build` succeeds
