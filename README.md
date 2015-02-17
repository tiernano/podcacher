# Podcacher
Application that caches Podcasts locally for use on different machines inside your network

The idea is quite simple. Podcatcher listens on a given url, example would be:

```
http://podcacherserver/feed?url=http://www.pwop.com/feed.aspx?show=dotnetrocks&filetype=master
```

in te background, podcacher will check if that feed already exists. if it does, it will return a cached version, with updated links to local files.

if not, it will download the xml, and store it locally. it will then find the last 10 feed items, download them in the background and save them to a serving folder.

finally, when a podcasting client (iTunes, Podcasts on iOS, etc) tries to download the file, it is served from the podcacher server, not the upstream provider.

urls for your podcasts will need to be changed to include the new address above. **This is not the final url**. We are still thinking about this...