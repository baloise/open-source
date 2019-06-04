![](https://upload.wikimedia.org/wikipedia/commons/thumb/8/89/Icon_DINA_Voraussetzungen_Digitale_Nachhaltigkeit_01_Ausgereift_Farbig.svg/200px-Icon_DINA_Voraussetzungen_Digitale_Nachhaltigkeit_01_Ausgereift_Farbig.svg.png)

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

If you are behind a corporate proxy you may have to [disable the SSL verification](https://git-scm.com/docs/git-config#Documentation/git-config.txt-httpsslVerify) for git.

## [release engineering](https://en.wikipedia.org/wiki/Release_engineering)

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

## project metrics

Such metrics may be related to your builds, chats, dependencies, sizes, downloads, funding, issue tracking, licenses, rating, social media, versioning, platform and version support, monitoring and more.

### highlight important stats with [badges from shields.io](https://shields.io) e.g. ![GitHub stars](https://img.shields.io/github/stars/badges/shields.svg?style=social&label=Stars)
