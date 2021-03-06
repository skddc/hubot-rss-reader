Hubot RSS Reader
================
RSS Reader for each Chat Channels, works with Hubot.

[![Build Status](https://travis-ci.org/shokai/hubot-rss-reader.svg?branch=master)](https://travis-ci.org/shokai/hubot-rss-reader)

- https://github.com/shokai/hubot-rss-reader
- https://www.npmjs.org/package/hubot-rss-reader

![screen shot](http://gyazo.com/234dfb14d76bb3de9efd88bfe8dc6522.png)

Requirements
------------

- redis-brain
- coffee-script 1.8+


Install
-------

    % npm install hubot-rss-reader -save
    % npm install coffee-script@">=1.8.0" -save

### edit `external-script.json`

```json
["hubot-rss-reader"]
```

### Configure (ENV var)

    export HUBOT_RSS_INTERVAL=600      # 600 sec (default)
    export HUBOT_RSS_HEADER=:sushi:    # RSS Header Emoji (default is "sushi")
    export HUBOT_RSS_USERAGENT=hubot   # (default is "hubot-rss-reader/#{package_version}")
    export DEBUG=hubot-rss-reader*     # debug print
    export HUBOT_RSS_PRINTSUMMARY=true # print summary (default is "true")

Usage
-----

### add

    hubot rss add https://github.com/shokai.atom
    # or
    hubot rss register https://github.com/shokai.atom


### delete

    hubot rss delete https://github.com/shokai.atom
    hubot rss delete #room_name

### list

    hubot rss list
    hubot rss dump


Test
----

    % npm install

    % grunt
    # or
    % npm test
