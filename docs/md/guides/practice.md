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

### building

### releasing

### publishing
