# OSINT Cheatsheet

## Information Searching Essentials
### Capturing Content 
#### Screenshots
It is important to record any information and online content that helps to address your information requirements. Your collection plan is a great place to document the sorts of content you expect to find and collect - this might include images, videos, text, URLs, social media posts and comments, news and journal articles, usernames, avatars, HTML code, and much more.
| Command / Query | Description |
| --- | --- |
| `Win + Shift + S` | Take a screenshot on Windows. |
| `Com + Shift + 4` | Take a screenshot on Mac. |
| `Right Click + Take Screenshot` | Capture an entire page on Firefox. |
#### Twitter / X
| Command / Query | Description |
| --- | --- |
| `https://tweetbeaver.com/` | Contains several tools that allow you to download selected information from Twitter and export it as a CSV if required. |
| `https://pypi.org/project/twint/` | Twint has a lot of features for capturing specific kinds of information and integrates nicely with some common visualisation tools. It doesn’t use the Twitter API and it’s really powerful. |
#### YouTube-dl
| Command / Query | Description |
| --- | --- |
| `youtube-dl <url>` | Use YouTube-dl to download a YouTube, Facebook or Twitter video via the CLI. |

### Boolean Searching
Boolean operators are words (or symbols) that assist in refining or expanding the parameters of your search. The three main Boolean operators we can use in Google, Bing, and other search engines are AND, OR, and - (the minus symbol).
| Command / Query | Description |
| --- | --- |
| `<search term> AND <search term>` | Search Google and only show results that include **all** search terms or key words. |
| `<search term> OR <search term>` | Search Google and include results that include **either** of the search terms or key words. |
| `<search term> -<search term>` | Use the **minus symbol (-)** to not include that specific search term. This can also extend to website (i.e. do not include results from facebook.com). |

### Advanced Google Searching (Dorking)
Google has a series of in-built advanced search operators that can be used to refine or expand searches (in addition to Boolean operators). Using these operators is sometimes referred to as Google 'Dorking'.
| Query | Description |
| --- | --- |
| `site:` | Only search within this websites given domain e.g., site:thehackernews.com Russia |
| `filetype:` | Search only for files, not webpages e.g., moon landing filetype:PDF |
| `intitle:` | Search for various keywords inside the title, e.g., intitle: infosec |
| `intext:` | Search the body of a webpage for specific text e.g., "bad rabbit" ransomware |
| `related:` | Find websites that are related to your search term e.g., related:vk.com |
| `link:` | Find other pages indexed by Google that reference this link e.g., link:https://fbi.gov |
| `"quote"` | Find an exact phrase e.g., "''khorasan group" |
| `*` | Wildcard. Search for anything between these two words, but include both e.g., "J* Biden" |
| `before:` `after:` | Return results before & after a date. You must provide year-month-day dates or only a year e.g., "terrorist attack" after:2019-03-01 |

### Dark Web Searching
| Command / Query | Description |
| --- | --- |
| `http://juhanurmihxlp77nkq76byazcldy2hlmovfu2epvl5ankdibsot4csyd.onion/` | Ahmia search engine. |
| `http://haystak5njsmn2hqkewecpaxetahtwhsbsa64jom2k22z5afxhnpxfid.onion/` | Haystak search engine. |
| `http://darkschn4iw2hxvpv2vy2uoxwkvs2padb56t3h4wqztre6upoc5qwgid.onion` | Darksearch search engine, specifically made for cybersecurity searches. |
| `http://mlyusr6htlxsyc7t2f4z53wdxh3win7q3qpxcrbam6jf3dmua7tnzuyd.onion/captcha` | Kilos search engine, specifically made to find markets & vendor sold goods. |
| `http://phobosxilamwcg75xt22id7aywkzol6q6rfl2flipcqoc4e4ahima5id.onion/` | Phobos search engine, specifically made for multilingual searching. |
| `http://quosl6t6c64mnn7d.onion/` | Quo search engine. |
| `http://3bbad7fauom4d6sgppalyqddsqbf5u5p56b5k5uk2zxsy3d6ey2jobad.onion/` | OnionLand search engine for hidden services. |

### Reverse Image Searching
Reverse image searching involves providing the search engine with an image to find it's original source or locate where-else it appears on the internet.
| Command / Query | Description |
| --- | --- |
| `https://addons.mozilla.org/en-GB/firefox/addon/search_by_image/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search` | Use this plug-in to reverse image search with Google, Bing, Yandex, Baidu and TinEye. |

### Contact Validation with Emails
The primary focus is on verifying contact information, especially email addresses, discovered during OSINT investigations.
| Command / Query | Description |
| --- | --- |
| `https://emailrep.io` | Used to analyse an email's digital footprint based on various factors like domain age, traffic rankings, social media presence, data breaches and more. |
| `https://haveibeenpwned.com` | Used to analyse if an email or mobile number is included in a data breach. |
| `https://phonebook.cz` | Requiring an account, this tool provides data on domains, email addresses, and URLs associated with a given input. |
| `https://whoxy.com` | A comprehensive domain name research tool offering information about a domain's ownership, registration history, and associated email accounts. |
| `https://viewdns.info` | This versatile platform provides multiple tools. One standout feature is its ability to reverse engineer domain names using an email address, which helps in mapping a subject's digital footprint across different websites. |

### Threat Intelligence
| Command / Query | Description |
| --- | --- |
| `https://urlscan.io` | Scan and analyse webpages, helps determine whether the site is malicious or not and gathers other useful information. |
| `https://abuse.ch` | Hunt for malware and botnets. Includes the services: Malware Bazaar, Feodo Tracker (botnets), SSL Blacklist, URL Haus, Threat Fox & Yara IFY. |

### Find Wi-Fi Networks
| Command / Query | Description |
| --- | --- |
| `https://wigle.net` | Use this service to find Wi-Fi networks by BSSID, IP address etc. |

### Open/Public Cloud Storage
| Command / Query | Description |
| --- | --- |
| `intext:<search-term> inurl:amazonaws.com` | Use Google Dorking to find if the target company/person is hosting storage in AWS. |
| `intext:<search-term> inurl:blob.core.windows.net` | Use Google Dorking to find if the target company/person is hosting storage in Azure blog storage. |
| `https://buckets.grayhatwarfare.com/` | Use this resource to query open/public cloud storage buckets. You can either manually search or enter buckets that you have found while Google dorking. |


---
## Passive Information Gathering (eJPT Content)
### Web Recon & Footprinting
| Command / Query | Description |
| --- | --- |
| `whatweb <domain>` | Used for both passive and aggressive information gathering of web technologies of a website. |
| `https://httrack.com` | Used to download a website to your local directory for offline source code analysis. |
| `whois <domain>` | Used to find out DNS information, including regristrar information/contacts, name servers, DNSSEC. |
| `https://netcraft.com/internet-data-mining` | Used to find web technologies running, DNS/registrar information, IP delegations, certificate transparency and SSL vulnerabilities in one place. Scroll to the bottom of the page to find the search box needed. |

### DNS Recon
| Command / Query | Description |
| --- | --- |
| `dnsrecon -d <domain>` | A python script that checks name server records for zone transfers, general DNS records (MX, A, AAAA, TXT etc.) and SRV record enumeration. |
| `https://dnsdumpster.com` | Same as dnsrecon but sorts and organises information in a clearer and more understandable layout. Also includes subdomains. *AMAZING* |

### Subdomain Enumeration
| Command / Query | Description |
| --- | --- |
| `https://dnsdumpster.com` | Includes subdomains associated to the website. |
| `sublist3r -d <domain>` | Used to perform passive subdomain enumeration. |

### Email Harvesting
| Command / Query | Description |
| --- | --- |
| `theHarvester -d <domain>` | Used to find email addresses associated with an organisation's domain. |
| `theHarvester -d <domain> -b dnsdumpster` | Use theHarvester to query dns dumpster. |


---
## Australian Information Sources and Collection
### Australia-Wide
| Command / Query | Description |
| --- | --- |
| `https://personlookup.com.au` | 8 million records including historic address information and telephone numebers. |
| `https://yellowpages.com.au` | Business listings, phone numbers, maps, email addresses & websites for local Australian businesses. |
| `https://whitepages.com.au` | Search for Australian businesses. |
| `https://abr.business.gov.au/` | ABN Lookup. |
| `https://realestate.com.au` | Property lookup. |
| `https://auccr.com/free` | Criminal court records. |
| `https://db.ccrau.com.au/free` | Civil court records. |
| `https://db.socr.com.au/free` | Sex offender search. |
| `https://db.dvos.com.au` | Domestic violence check. |

### ACT
| Command / Query | Description |
| --- | --- |
| `https://www.courts.act.gov.au/magistrates/lists` | ACT daily court lists. |

### NSW
| Command / Query | Description |
| --- | --- |
| `https://service.nsw.gov.au/transaction/check-vehicle-registration` | Check vehicle registration for NSW license plates. |
| `https://onlineregistry.lawlink.nsw.gov.au/Landing.html?redir=/content/court-lists%3f` | NSW daily court lists. |

### NT
| Command / Query | Description |
| --- | --- |
| `https://nt.gov.au/driving/rego/check,-renew-or-transfer-your-registration/rego-check` | Check vehicle registration for NT license plates. |
| `https://justice.nt.gov.au/courts/magistrates-court-daily-court-list` | NT daily court lists. |

### QLD
| Command / Query | Description |
| --- | --- |
| `https://service.transport.qld.gov.au/checkrego/application/TermAndConditions.xhtml?dswid=5326` | Check vehicle registration for QLD license plates. |
| `https://www.courts.qld.gov.au/daily-law-lists/daily-law-lists` | QLD daily court lists. |

### SA
| Command / Query | Description |
| --- | --- |
| `https://www.transport.tas.gov.au/MRSWebinterface/public/regoLookup/registrationLookup.jsf` | Check vehicle registration for SA license plates. |
| `https://www.courts.sa.gov.au/case-lists/all-criminal-cases/` | SA daily court lists. |

### TAS
| Command / Query | Description |
| --- | --- |
| `https://www.transport.tas.gov.au/MRSWebInterface/public/regoLookup/registrationLookup.jsf` | Check vehicle registration for TAS license plates. |
| `https://www.magistratescourt.tas.gov.au/lists` | TAS daily court lists. |

### VIC
| Command / Query | Description |
| --- | --- |
| `https://vicroads.vic.gov.au/registration/buy-sell-or-transfer-a-vehicle/check-vehicle-registration/vehicle-registration-enquiry` | Check vehicle registration for VIC license plates. |
| `https://dailylists.magistratesvic.com.au/EFAS/CaseSearch` | VIC daily court lists. |

### WA
| Command / Query | Description |
| --- | --- |
| `https://online.transport.wa.gov.au/webExternal/registration/;jsessionid=YMvghLiTpzCFbJ2VLru7SBwMiTkLX_RY2_5XBigMAMDLFD6NSK2v1-12780694141-578962984?0` | Check vehicle registration for WA license plates. |
| `https://ecourts.justice.wa.gov.au//eCourtsPortal/CourtListings/TodaysCourtListings` | WA daily court lists. |


---
## Tool-Specific Cheatsheets
### Capturing Content
#### Twint [Twitter/X]
| Command / Query | Description |
| --- | --- |
| `twint -u username` | Scrape all the Tweets from user's timeline. |
| `twint -u username -s pineapple` | Scrape all Tweets from the user's timeline containing pineapple. |
| `twint -s pineapple` | Collect every Tweet containing pineapple from everyone's Tweets. |
| `twint -u username --year 2014` | Collect Tweets that were tweeted before 2014. |
| `twint -u username --since "2015-12-20 20:30:15"` | Collect Tweets that were tweeted since 2015-12-20 20:30:15. |
| `twint -u username --since 2015-12-20` | Collect Tweets that were tweeted since 2015-12-20 00:00:00. |
| `twint -u username -o file.txt` | Scrape Tweets and save to file.txt. |
| `twint -u username -o file.csv --csv` | Scrape Tweets and save as a csv file. |
| `twint -u username --email --phone` | Show Tweets that might have phone numbers or email addresses. |
| `twint -s "Donald Trump" --verified` | Display Tweets by verified users that Tweeted about Donald Trump. |
| `twint -g="48.880048,2.385939,1km" -o file.csv --csv` | Scrape Tweets from a radius of 1km around a place in Paris and export them to a csv file. |
| `twint -u username -es localhost:9200` | Output Tweets to Elasticsearch |
| `twint -u username -o file.json --json` | Scrape Tweets and save as a json file. |
| `twint -u username --database tweets.db` | Save Tweets to a SQLite database. |
| `twint -u username --followers` | Scrape a Twitter user's followers. |
| `twint -u username --following` | Scrape who a Twitter user follows. |
| `twint -u username --favorites` | Collect all the Tweets a user has favorited (gathers ~3200 tweet). |
| `twint -u username --following --user-full` | Collect full user information a person follows. |
| `twint -u username --profile-full` | Use a slow, but effective method to gather Tweets from a user's profile (Gathers ~3200 Tweets, Including Retweets). |
| `twint -u username --retweets` | Use a quick method to gather the last 900 Tweets (that includes retweets) from a user's profile. |
| `twint -u username --resume resume_file.txt` | Resume a search starting from the last saved scroll-id. |

#### YouTube-dl [YouTube/Facebook/Twitter/X]
| Command / Query | Description |
| --- | --- |
| `sudo -H pip install --upgrade youtube-dl` | Install snapd. |
| `youtube-dl -h` | Show the help options for YouTube-dl. |
| `youtube-dl <url>` | Download a video. |


### Metadata
#### Exiftool
| Command / Query | Description |
| --- | --- |
| `exiftool -a <filename>` | Analyse **all** of a files' metadata with exiftool. |


### Person Enumeration
#### spiderfoot
| Command / Query | Description |
| --- | --- |
| `python3 ./sf.py -l 127.0.0.1:5001` | After moving to the relevant folder, run the spiderfoot script and then navigate to it in your browser. |
| `spiderfoot -l 127.0.0.1:5001` | Alternatively, run the Kali native version of spiderfoot. |
**Module options on Spiderfoot for personell checking:**
1. Social Network Identifier
2. DuckDuckGo
3. Account Finder
4. Instagram
5. Ahmia


---
## How to Submit Evidence
For the National Missing Persons Hackathon 2024.
| Path | Description |
| --- | --- |
| `Investigations > Cases` | Add a piece of evidence at this path. The entries can be written in **mark down language**. The date field is *not* mandatory.  |
