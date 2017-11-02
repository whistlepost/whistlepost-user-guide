---
layout: post
title:  "Getting started!"
date:   2016-11-04 05:05:26 +0000
categories: beginner
---

[Lazybones]: https://github.com/pledbrook/lazybones
[SDKMAN]: http://sdkman.io/

Whistlepost provides a [Lazybones] project template that is probably the simplest way to create a new Whistlepost site.
The following steps outline how to use it:

1. Install [Lazybones] via [SDKMAN]:

	```$ curl -s "https://get.sdkman.io" | bash && sdk install lazybones```

1. Include the Whistlepost repository in configuration:

	```$ lazybones set bintrayRepositories = [micronode/whistlepost, pledbrook/lazybones-templates]```

1. Create a new site skeleton using the Whistlepost template:

	```$ lazybones create whistlepost-site <site directory>```
