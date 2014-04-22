---
layout: midnight
title: FreeNAS notes
---

FreeNAS
=======

Potential fix for [too many open files](https://bugs.freenas.org/issues/4402) bug:

```ini
# Probably not needed
change notify = no
# Most likely required
kernel change notify = no
```

Enabling [NFSv4 support](https://bugs.freenas.org/issues/3546) in 9.2.x:

`touch /etc/nfsv4_enable && mountrw / && touch /conf/base/etc/nfsv4_enable && mount -ur /`
