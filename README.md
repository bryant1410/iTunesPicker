iTunesPicker 2.1.1
============

A complete App to discover, search and compare world rankings for apps, ibooks, movies and music **from iTunes in any available country**. iTunesPicker show app price drops from [appcorner.it](http://www.appcorner.it/en/), take a look to [AppCorner Social](https://github.com/appcornerit/AppCorner-Social) you can create a website with your favorites apps or price drops.

Charts supported by the current version:
iOS Apps, iPad Apps, Mac Apps, Music (Song and Albums), Music Videos, iBooks, Movies.

Search Music, Movies and Music Videos on YouTube.

iTunesPicker is for iPhone only, requires iOS 7 or above and use **AppCornerKit framework** that simplifies communication with iTunes API, the framework is included in the external folder and is free for unlimited use.

**Author**: Denis Berton [@DenisBerton](https://twitter.com/DenisBerton)

![Alt text](preview/4.0/1.png "Preview songs") 

#### Publish on App Store
iTunesPicker is not published on the App Store by appcorner.it, **you're free to publish this version "as is" on App Store** or with your changes (please quote this repository in the app description).

The app "as is" could not pass the approval rules of App Store:
- rule 8.1 cannot contain "iTunes" in the app name
- rule 8.3 could be evaluated similar to iTunes
- rule 2.25 you should remove apps ranking.


#### Configuration
To enable remote configuration (to hide/show items types in app) set on iTunesPicker-Prefix.pch
```objc
#define REMOTE_CONFIGURATION_ENABLE 1
#define REMOTE_CONFIGURATION_SERVER_URL @"http://example.com/defaults.plist" //upload the file on your server
#define DEFAULT_ACK_TYPES @[@(kITunesEntityTypeSoftware),@(kITunesEntityTypeMusic),@(kITunesEntityTypeEBook),@(kITunesEntityTypeMovie)]; //change types loaded by default on first time (offline) 
```

To enable YouTube search, add your api key in iTunesPicker-Prefix.pch
```objc
#define YOUTUBE_API_KEY @""
```

You can share your favorite apps (or build your AppCornerKit framework from scratch), take a look to [AppCorner Social](https://github.com/appcornerit/AppCorner-Social), iTunesPicker can share apps on AppCorner Social.
