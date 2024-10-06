---
title: Client Setup
description: 
published: true
date: 2024-10-06T14:29:18.068Z
tags: 
editor: markdown
dateCreated: 2021-09-20T14:45:08.138Z
---

# Client Setup
## 3.3.5a
1. Open the realmlist.wtf file inside your World of Warcraft\Data\enUS folder. The IP in the realmlist.wtf file should be exactly the same as the IP address you entered in the realmlist table above.

- Change the first line to: **set realmlist** IP address used in realmlist table
- Example: **set realmlist 127.0.0.1**
> (Optional) If you wish to use the WoW Launcher.exe to run your client then you must change your set patchlist to the same ip/dns name as your realmlist.

## Master, cata_classic (wow 4.4.x)
1. Change Config.wtf: **SET portal** "IP address used in realmlist table"
- The IP in the Config.wtf file should be exactly the same as the IP address you entered in the - realmlist table above. (Example: **SET portal "127.0.0.1"**)
> Note: you will need a custom client launcher to connect to master, cata_classic branches servers, i.e. https://arctium.io/wow

> Supported Version
Check https://github.com/TrinityCore/TrinityCore to find the exact client version supported by master branch.
{.is-info}

> NOTE don't use localhost for address, if you need to connect to localhost use 127.0.0.1
{.is-warning}

  ##  Help

If you still have any problem, check:

- Updating or starting with TrinityCore issues, Trouble with your TrinityCore Install / Readme 1st / FAQs
- [Ask help on the Forum.](https://talk.trinitycore.org/)
- If you still have problems, you can try to ask help on [Discord](https://discord.com/invite/HPP3wNh), but remember it's not real time 24/7 support, most of people there lives on GMT and they can be sleeping or working.
