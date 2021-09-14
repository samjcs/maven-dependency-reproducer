# maven-dependency-reproducer
Test Project to reproduce a bug in the Maven Dependecy plugin

# Reproduce

Run

    mvn org.apache.maven.plugins:maven-dependency-plugin:<version>T:tree -Dverbose

where `<version>` is the local build that you want to test.

using `git bisect` on the plugin sources, I found the offending commit which is https://github.com/apache/maven-dependency-plugin/commit/10398ddae456ad921e361f822e80a7d05bf1279a .
