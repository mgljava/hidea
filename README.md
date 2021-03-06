# Hbase Plugin for IntelliJ IDEA

## Description
Provide simple querying interface of hbase tables. This plugin is mainly used for development/testing purposes(especially local development databases), so a full
list of configuring options might not be supported. Use at your own risk!

## Installing
Just install the zip under snapshots/ to your intellij idea

## Debugging instructions
1. Set up development environment according to instructions [here](http://www.jetbrains.org/intellij/sdk/docs/basics/getting_started/setting_up_environment.html)
1. Open the project dir from intellij idea
1. Run the 'Plugin' target from intellij idea

## Building with maven
1. install following libs to your local maven repo:

        mvn install:install-file -Dfile=forms_rt.jar -DgroupId=com.intellij -DartifactId=forms_rt -Dversio=14.1 -Dpackaging=jar
        mvn install:install-file -Dfile=forms_rt.jar -DgroupId=com.intellij -DartifactId=forms_rt -Dversion=14.1 -Dpackaging=jar
        mvn install:install-file -Dfile=openapi.jar -DgroupId=com.intellij -DartifactId=openapi -Dversion=14.1 -Dpackaging=jar
        mvn install:install-file -Dfile=jna.jar -DgroupId=com.intellij -DartifactId=jna -Dversion=14.1 -Dpackaging=jar
        mvn install:install-file -Dfile=util.jar -DgroupId=com.intellij -DartifactId=util -Dversion=14.1 -Dpackaging=jar
        mvn install:install-file -Dfile=idea.jar -DgroupId=com.intellij -DartifactId=idea -Dversion=14.1 -Dpackaging=jar
        mvn install:install-file -Dfile=extensions.jar -DgroupId=com.intellij -DartifactId=extensions -Dversion=14.1 -Dpackaging=jar
        mvn install:install-file -Dfile=resources.jar -DgroupId=com.intellij -DartifactId=resources -Dversion=14.1 -Dpackaging=jar
        mvn install:install-file -Dfile=resources_en.jar -DgroupId=com.intellij -DartifactId=resources_en -Dversion=14.1 -Dpackaging=jar
        mvn install:install-file -Dfile=icons.jar -DgroupId=com.intellij -DartifactId=icons -Dversion=14.1 -Dpackaging=jar
        
1. set up properties intellij.sdk.name, intellij.sdk.version, intellij.sdk.path, etc in pom.xml according to your configuration.
1. mvn clean package
1. It seems that there are some problems building with JDK8. If you managed get it to build with JDK8 please tell me.

## TODO
1. Support editing, deleting and copying values
1. Support filtering by columns

## Acknowlegement
[mongo4idea](https://github.com/dboissier/mongo4idea) a great reference of Intellij Idea plugin development.

