---
title: "Demo Post"
date: 2022-12-14T13:20:07-08:00
draft: false
---
## GemFire
The getKeySet method:
* creates a proxy Region connected to the input site
* gets the keySet for the Region on that site using keySetOnServer
closes the Region
* The getKeySet method is invoked for each site.

```java
private Set getKeySet(String regionName, String siteName) {
 Region region = createRegion(regionName, siteName);
 Set keySet = region.keySetOnServer();
 closeRegion(region);
 return keySet;
}
```

![diagram](https://content.cdntwrk.com/files/aHViPTYzOTc1JmNtZD1pdGVtZWRpdG9yaW1hZ2UmZmlsZW5hbWU9aXRlbWVkaXRvcmltYWdlXzVmZTBlOTRhM2MwMTcucG5nJnZlcnNpb249MDAwMCZzaWc9YzYzNWIzYWFhMzQwYzJjZDQwZDU0ODNiYmZiN2I2ZTE%253D)