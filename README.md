Gradle Lock Bom Example
=======================

Lock files generated with `./gradlew dependencies --write-locks`

Branch: master
--------------

* Uses [nebula.dependency-recommender](https://plugins.gradle.org/plugin/nebula.dependency-recommender)
* `./gradlew build` succeeds as of 4.8-20180428001031+0000

Branch: new-bom-support
-----------------------

* Uses `enableFeaturePreview('IMPROVED_POM_SUPPORT')` in settings.gradle
* `./gradlew build` succeeds

Branch: use-version
-------------------

* `./gradlew build` succeeds
* `./gradlew dependencies` succeeds as of 4.8-20180428001031+0000

