![](https://upload.wikimedia.org/wikipedia/commons/thumb/8/89/Icon_DINA_Voraussetzungen_Digitale_Nachhaltigkeit_01_Ausgereift_Farbig.svg/200px-Icon_DINA_Voraussetzungen_Digitale_Nachhaltigkeit_01_Ausgereift_Farbig.svg.png)

# practice

## access from corporate context

### behind a proxy

#### Recommendation: use a local proxy (e.g. [this one](https://github.com/baloise/proxy#installation)) and chain this to your corporate proxy.
#### Advantage: cross application, unified local proxy settings for in- and external traffic rules

Simply configure within all applications your local "ProxyChain". For e.g. git you have to configure your `git --global -l` .gitconfig like

```
[url "http://"]
	insteadOf = git://
[http]
	sslVerify = false
	proxy = "http://localhost:8888"
[https]
        sslVerify = false
	proxy = "http://localhost:8888"
```

e.g. by using the following commands

```
git config --global url."http://".insteadOf git://

// ProxyProxy setting(s)
git config --global http.sslVerify false
git config --global http.proxy "http://localhost:8888"

git config --global https.sslVerify false
git config --global https.proxy "http://localhost:8888"
```

## [release engineering](https://en.wikipedia.org/wiki/Release_engineering)

### building

#### [Travis-CI](../activities/profiles.md#travis-ci)
 - [Getting started](https://docs.travis-ci.com)

### releasing
#### [Github Releases](https://help.github.com/articles/creating-releases/)
Create releases to bundle and deliver iterations of a project to users.

#### [Maven Release Plugin](http://maven.apache.org/maven-release/maven-release-plugin/)
A plugin to release a project with Maven, saving a lot of repetitive, manual work.

#### [semantic-release](https://semantic-release.gitbook.io/semantic-release/)
Fully automated version management and package publishing. Highlights:
 - Determine the next semantic version number based on [commit messages](https://semantic-release.gitbook.io/semantic-release/#commit-message-format)
 - Create Git tags and release notes
 - Publish artifacts
 - High extensibility through a large number of plugins, e.g.
   - [Github plugin](https://github.com/semantic-release/github): Create Github releases and comment on PRs, Issues, etc.
   - [Changelog plugin](https://github.com/semantic-release/changelog): Create a changelog file
   - [Docker plugin](https://github.com/felixfbecker/semantic-release-docker): Publish to docker registry
   - [Exec plugin](https://github.com/semantic-release/exec): Run custom scripts

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
