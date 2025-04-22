# lazycat netdata

Port [netdata](https://www.netdata.cloud/) to lazycat store.

## Steps to follow upstream version

1. clone container image to lazycat official registry

```bash
# replace v2.4.0 with the version you want to clone
$ lzc-cli appstore copy-image netdata/netdata:v2.4.0
Waiting ... ( copy netdata/netdata:v2.4.0 to lazycat offical registry)
lazycat-registry: registry.lazycat.cloud/u11408144/netdata/netdata:99ad366ae2ca587f
```

2. update lzc-manifest.yaml

3. build project

```bash
$ lzc-cli project build
跳过执行 buildscript
跳过拷贝 contentdir 内容
输出lpk包 /Users/strrl/playground/GitHub/lazycat-netdata/cloud.lazycat.app.netdata-v2.4.0-1.lpk
```

4. publish lpk

```bash
$ lzc-cli appstore publish ./cloud.lazycat.app.netdata-v2.4.0-1.lpk
```

5. wait for review

developer portal: <https://developer.lazycat.cloud/manage>
