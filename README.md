# saas_cnc

This is a project for the DefCon [Cloud Village](https://cloud-village.org), demonstrating just how easy it is for attackers and malware authors to use SaaS and social media services as command and control vectors.

**This code is a proof of concept intended for research purposes only. It does not contain any payloads.  It is not weaponized.**

Design was in no small part influenced by:
* The Slub Backdoor as reported by [Trend Micro](https://blog.trendmicro.com/trendlabs-security-intelligence/new-slub-backdoor-uses-github-communicates-via-slack/) and us at [Netskope](https://www.netskope.com/blog/slubs-the-word-covert-cnc-over-slack)
* PaulSec's [Twittor](https://github.com/PaulSec/twittor)
* Coalfire's [Slackor](https://www.coalfire.com/The-Coalfire-Blog/June-2019/Introducing-Slackor)

We leverage the following apps/services:

**Retrieving API keys**
* Github Gist
* Pastebin

**Command and Control**
* Slack
* Twitter
* Github

**File Exfiltration**
* Slack
* Imgur (images only)
* Dropbox
* File.io

They key here is that we're looking to be robust to changing API keys, getting banned from platforms, and from IDS/IPS.
The weakness that can be exploited is that the initial fetching of API keys from Github and Pastebin necessitates that those locations be hard-coded. 
There are some potential workarounds there (including maybe just hard-coding the API keys for Slack from the start!).

**Again, this code is a proof of concept intended for research purposes only. It does not contain any payloads.  It is not weaponized.**
