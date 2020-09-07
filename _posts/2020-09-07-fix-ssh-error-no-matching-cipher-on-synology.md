---
layout: post
title:  "How to fix broken SSH on Synology DSM (no matching cipher found)"
date:   2020-09-07 14:36:00 +0000
categories: snippets
---

Whilst trying to log-in to my **Synology DS414** NAS today via SSH I was greeted with this error:

`Unable to negotiate with 192.168.0.xxx port xxx: no matching cipher found. Their offer: aes128-cbc,3des-cbc,aes192-cbc,aes256-cbc`

I am running DSM version 6.2.2-24922 Update 4 (although 6.2.3-25426 is available as an update).

It would appear that since I last attempted to log in, Synology have changed their security settings.

To fix this I found a helpful blog post by [Mattias Geniar](https://ma.ttias.be/ssh-error-unable-negotiate-ip-no-matching-cipher-found/). 

His solution that worked for me was to go to Control Panel in Synology DSM, then choose from the left-hand column "Terminal & SNMP" > "Terminal", and then change the value to "High". 

After applying the setting SSH is back working again with no errors.

Screenshots below:

![DSM Control Panel > Terminal & SNMP > Terminal screen](/images/synology-dsm-how-to-fix-ssh-error-no-matching-cipher-found-1.png){:class="img-responsive"}

![Advanced Settings panel](/images/synology-dsm-how-to-fix-ssh-error-no-matching-cipher-found-2.png){:class="img-responsive"}

[Let me know](https://twitter.com/hobbsy) if this works for you too. Thanks Mattias for the tip!

Related links:  
* [DSM Release Notes for DS414](https://www.synology.com/en-gb/releaseNote/DS414)
* [Synology Download Centre for DS414](https://www.synology.com/en-gb/support/download/DS414)
