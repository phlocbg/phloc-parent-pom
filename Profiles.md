# Default profile #

  * Assigns default version number for a small number of artefacts (junit, slf4j, jsp-api and servlet-api)
  * Always depends on JUnit 4.10 in scope _test_
  * Defines other repositories where artefacts should be looked up
  * Supported build plugins are
    * com.mycila.maven-license-plugin:maven-license-plugin
    * org.apache.felix:maven-bundle-plugin
    * org.apache.maven.plugins:maven-antrun-plugin
    * org.apache.maven.plugins:maven-assembly-plugin
    * org.apache.maven.plugins:maven-clean-plugin
    * org.apache.maven.plugins:maven-compiler-plugin
    * org.apache.maven.plugins:maven-dependency-plugin
    * org.apache.maven.plugins:maven-deploy-plugin
    * org.apache.maven.plugins:maven-ear-plugin
    * org.apache.maven.plugins:maven-ejb-plugin
    * org.apache.maven.plugins:maven-gpg-plugin
    * org.apache.maven.plugins:maven-install-plugin
    * org.apache.maven.plugins:maven-jar-plugin
    * org.apache.maven.plugins:maven-jarsigner-plugin
    * org.apache.maven.plugins:maven-javadoc-plugin
    * org.apache.maven.plugins:maven-jxr-plugin
    * org.apache.maven.plugins:maven-plugin-plugin
    * org.apache.maven.plugins:maven-pmd-plugin
    * org.apache.maven.plugins:maven-project-info-reports-plugin
    * org.apache.maven.plugins:maven-rar-plugin
    * org.apache.maven.plugins:maven-release-plugin
    * org.apache.maven.plugins:maven-resources-plugin
    * org.apache.maven.plugins:maven-site-plugin
    * org.apache.maven.plugins:maven-source-plugin
    * org.apache.maven.plugins:maven-surefire-plugin
    * org.apache.maven.plugins:maven-surefire-report-plugin
    * org.apache.maven.plugins:maven-war-plugin
    * org.codehaus.mojo:cobertura-maven-plugin
    * org.codehaus.mojo:dashboard-maven-plugin
    * org.codehaus.mojo:findbugs-maven-plugin
    * org.codehaus.mojo:jdepend-maven-plugin
    * org.codehaus.mojo:taglist-maven-plugin
    * com.phloc.maven:buildinfo-maven-plugin
    * com.phloc.maven:closure-maven-plugin
    * com.phloc.maven:csscompress-maven-plugin
    * org.eclipse.m2e:lifecycle-mapping
  * It uses the Wagon extensions for http, ssh and file
  * Default configurations are provided for:
    * maven-compiler-plugin
    * maven-source-plugin
    * maven-jar-plugin
    * maven-war-plugin
    * maven-license-plugin
    * maven-release-plugin
    * buildinfo-maven-plugin
    * maven-site-plugin

# Other profiles #

Besides the default profile, the following profiles are offered:
  * **release** a special profile to be used when releasing a software component (e.g. using the [maven-release-plugin](http://maven.apache.org/plugins/maven-release-plugin/)).
    * using optimized output of the maven-compiler-plugin
    * creates a checksum with the maven-install-plugin
    * signs artefacts using the maven-gpg-plugin
  * **hduson** for use in Hudson/Jenkins
    * Performs [FindBugs](http://findbugs.sourceforge.net/) analysis
    * Does coe coverage analysis with [Cobertura](http://cobertura.sourceforge.net/)
    * Exports the dependencies in XML format via maven-dependency-plugin
  * **jdk5** to build JAR files that are executable by Java 1.5
    * using the target _1.5_ for the maven-compiler-plugin
    * adds the classifier "jdk5" to the resulting artefacts

Read more on [Maven profiles](http://maven.apache.org/guides/introduction/introduction-to-profiles.html).