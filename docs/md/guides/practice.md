# practice

## access from corporate context 

### behind a proxy

#### Recommendation: use a local proxy (e.g. [this one](https://github.com/baloise/proxy#installation)) and chain this to your corporate proxy. 
#### Advantage: cross application, unified local proxy settings for in- and external traffic rules

Simply configure within all applications your local "ProxyChain".

```properties
# within: %userprofile%\.proxy\proxy.properties
# e.g. for Baloise

SimpleProxyChain.upstreamPort=3128
SimpleProxyChain.noproxyHostsRegEx=.*((baloise|baloisenet|balgroupit).com|bvch.ch|baloise.ch)\\Z
SimpleProxyChain.upstreamServer=webproxy
```

## [release engineering](https://en.wikipedia.org/wiki/Release_engineering)

### artifact / module attributes

#### Use ([semantic](https://semver.org)) version numbers
#### Include license file in binary distributions

### building

#### [Travis-CI](../activities/profiles.md#travis-ci)
 - [Getting started](https://docs.travis-ci.com)
 
### releasing
#### [Github Releases](https://help.github.com/articles/creating-releases/)
#### [Maven Release Plugin](http://maven.apache.org/maven-release/maven-release-plugin/)

### publishing

#### Maven artifacts
 - [Bintray](../activities/profiles.md#jfrog-bintray)
   - standard public maven repo
 - [JitPack.io](https://jitpack.io/docs/)
   - easy to use
   - namespace and IDs are derived repository URL (` != pom.xml` attribtues)
