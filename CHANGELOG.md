# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres to [Semantic Versioning](http://semver.org/).

<!-- Format restrictions - see https://common-changelog.org and https://keepachangelog.com/ for details -->
<!-- Each Release must start with a line for the release version of exactly this format: ## [version] -->
<!-- The subsequent comment lines start with a space - not to irritate the release scripts parser!
 ## [major.minor.micro]
 <empty line> - optional sub sections may follow like:
 ### Added:
 - This feature was added
 <empty line>
 ### Changed:
 - This feature was changed
 <empty line>
 ### Removed:
 - This feature was removed
 <empty line>
 ### Fixed:
 - This issue was fixed
 <empty line>
 <empty line> - next line is the starting of the previous release
 ## [major.minor.micro]
 <empty line>
 <...>
 !!! In addition the compare URL links are to be maintained at the end of this CHANGELOG.md as follows.
     These links provide direct access to the GitHub compare vs. the previous release.
     The particular link of a released version will be copied to the release notes of a release accordingly.
     At the end of this file appropriate compare links have to be maintained for each release version in format:
 
  +-current release version
  |
  |                   +-URL to this repo                previous release version tag-+       +-current release version tag
  |                   |                                                              |       |
 [major.minor.micro]: https://github.com/mavenplugins/maven-cdi-plugin-hooks/compare/vM.N.u..vM.N.u
-->
<!--
## [Unreleased]

### 🚨 Removed
- TBD

### 💥 Breaking
- TBD

### 📢 Deprecated
- TBD

### 🚀 New Features
- TBD

### 🐛 Fixes
- TBD

### ✨ Improvements
- TBD

### 🔧 Internal Changes
- TBD

### 🚦 Tests
- TBD

### 📦 Updates
- TBD

### 🔒 Security
- TBD

### 📝 Documentation Updates
- TBD
-->

## [Unreleased]

### Changes
- TBD


## [0.2.1]
<!-- !!! Align version in badge URLs as well !!! -->
[![0.2.1 Badge](https://img.shields.io/nexus/r/io.github.mavenplugins/cdi-plugin-hooks?server=https://s01.oss.sonatype.org&label=Maven%20Central&queryOpt=:v=0.2.1)](https://central.sonatype.com/artifact/io.github.mavenplugins/cdi-plugin-hooks/0.2.1)

### Summary
- Remove vulnerability warnings due to guava and Maven dependency - see **📦 Updates** for details.

### 📦 Updates
- pom.xml:
  - Update dependency `io.github.mavenplugins:cdi-plugin-utils:4.0.0` -> `io.github.mavenplugins:cdi-plugin-utils:4.0.1`
  - Remove explicit dependency to `com.google.guava:guava`
  - Update dependency `org.apache.maven.shared:maven-invoker:2.2` -> `org.apache.maven.shared:maven-invoker:3.1.0`
  - Update dependency `com.google.http-client:google-http-client:1.22.0` -> `com.google.http-client:google-http-client:1.46.1`
  - Update provided dependency `org.apache.maven:maven-core:3.3.9` -> `org.apache.maven:maven-core:3.8.1`

### 🔧 Internal Changes
- MavenHook.java:
  - follow up API change of `org.apache.maven.shared.invoker.InvocationRequest`

- HttpRequestHook.java:
  - replace usage of `Objects.firstNonNull(...)` by `MoreObjects.firstNonNull(...)`


## [0.2.0]
<!-- !!! Align version in badge URLs as well !!! -->
[![0.2.0 Badge](https://img.shields.io/nexus/r/io.github.mavenplugins/cdi-plugin-hooks?server=https://s01.oss.sonatype.org&label=Maven%20Central&queryOpt=:v=0.2.0)](https://central.sonatype.com/artifact/io.github.mavenplugins/cdi-plugin-hooks/0.2.0)

### Summary
- Update dependency `io.github.mavenplugins:cdi-plugin-utils:3.4.1` -> `io.github.mavenplugins:cdi-plugin-utils:4.0.0`
  - => work for Java 8, 11, 17, 21 by CDI WELD 4.0.3.Final with Jakarta Inject API

### Compatibility
- 👉 This release requires to be used with `unleash-maven-plugin >= v3.0.0` only! It will NOT work with former versions of `unleash-maven-plugin`<br>
  Reason: CDI dependencies did have been changed from Javax to Jakarta EE

### Updates
- pom.xml:
  - update dependency `io.github.mavenplugins:cdi-plugin-utils:3.4.1` -> `io.github.mavenplugins:cdi-plugin-utils:4.0.0`


## [0.1.2]
<!-- !!! Align version in badge URLs as well !!! -->
[![0.1.2 Badge](https://img.shields.io/nexus/r/io.github.mavenplugins/cdi-plugin-hooks?server=https://s01.oss.sonatype.org&label=Maven%20Central&queryOpt=:v=0.1.2)](https://central.sonatype.com/artifact/io.github.mavenplugins/cdi-plugin-hooks/0.1.2)

### Summary
- Improve and precise Maven dependencies
- Requires Java 1.8
- Update dependency `io.github.mavenplugins:cdi-plugin-utils:3.4.0` -> `io.github.mavenplugins:cdi-plugin-utils:3.4.1`
- Update provided dependency to Maven version `3.3.9` -> `3.8.1`

### Updates
- pom.xml:
  - update parent pom reference
  - compile for Java 1.8
  - improve and precise Maven dependencies
  - update dependency `io.github.mavenplugins:cdi-plugin-utils:3.4.0` -> `io.github.mavenplugins:cdi-plugin-utils:3.4.1`


## [0.1.1]
<!-- !!! Align version in badge URLs as well !!! -->
[![0.1.1 Badge](https://img.shields.io/nexus/r/io.github.mavenplugins/cdi-plugin-hooks?server=https://s01.oss.sonatype.org&label=Maven%20Central&queryOpt=:v=0.1.1)](https://central.sonatype.com/artifact/io.github.mavenplugins/cdi-plugin-hooks/0.1.1)

### Summary
- Initial release of this artifact with new groupId `io.github.mavenplugins`
- Codewise identical with `com.itemis.maven.plugins:cdi-plugin-hooks:0.1.1`<br>No more features nor changes
- Update dependency `com.itemis.maven.plugins:cdi-plugin-utils:3.0.0` -> `io.github.mavenplugins:cdi-plugin-utils:3.4.0`
- Released to Maven Central

### Updates
- pom.xml:
  - update parent pom reference
  - update groupId to `io.github.mavenplugins`
  - update dependency `com.itemis.maven.plugins:cdi-plugin-utils:3.0.0` -> `io.github.mavenplugins:cdi-plugin-utils:3.4.0`
  - update `version.java` `1.6` -> `1.7`
  - update URLs to fit with new repo location
  - remove obsolete profile disable-java8-doclint

- README.md:
  - add URLs for build badges


<!--
## []

### NeverReleased
- This is just a dummy placeholder to make the parser of GHCICD/release-notes-from-changelog@v1 happy!
-->

[Unreleased]: https://github.com/mavenplugins/maven-cdi-plugin-hooks/compare/v0.2.1..HEAD
[0.2.1]: https://github.com/mavenplugins/maven-cdi-plugin-hooks/compare/v0.2.0..v0.2.1
[0.2.0]: https://github.com/mavenplugins/maven-cdi-plugin-hooks/compare/v0.1.2..v0.2.0
[0.1.2]: https://github.com/mavenplugins/maven-cdi-plugin-hooks/compare/v0.1.1..v0.1.2
[0.1.1]: https://github.com/mavenplugins/maven-cdi-plugin-hooks/releases/tag/v0.1.1
