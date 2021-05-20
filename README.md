# FairTurnRSS

A Google Apps Script for an RSS feed to power an Alexa skill for taking fair turns for a daily chore.  
Supports the set of people to choose from and the name of the "thing" to do as GET parameters.

## Example

Commandline:
```
curl -L "https://script.google.com/macros/s/AKfycbzlooGEeaxy3IB6lUGN7EEPtRi4e48xOd4zk1jiCrCF82I5--CskCpUd2I2_TqQ9x5L9A/exec?option=KidOne&option=KidTwo&option=KidThree&title=turn%20to%20feed%20the%20dog"
```
The "-L" tells curl to follow links.  Google Web Scripts always use redirects.  
NOTE: Arguments should be URL Encoded when passed in.  From the example above "turn to feed the dog" was encoded to "turn%20to%20feed%20the%20dog".  You can use an [online encoder](https://www.urlencoder.org/) if you need.

Response:
```
<?xml version="1.0" encoding="UTF-8"?>
<rss version="2.0" xmlns:atom="https://www.w3.org/2005/Atom">
  <channel>
    <atom:link href="https://garble.org/rss" rel="self" type="application/rss+xml" />
    <title>RSS 2.0 Feed with Google Apps Script</title>
    <link>https://garble.org</link>
    <description>RSS 2.0 Feed</description>
    <language>en</language>
    <item>
      <title>Today is KidTwo's turn to feed the dog</title>
      <link>https://garble.org/#139</link>
      <description>Today is KidTwo's turn to feed the dog</description>
      <pubDate>Wed, 19 May 2021 19:29:51 +0000</pubDate>
      <guid>https://garble.org/#139</guid>
    </item>
  </channel>
</rss>
```

## Usage

You can either copy and deploy this yourself, or use the above URL directly without needing to deploy any code.  Whichever you choose, it takes the following arguments:

 - ***option***: Meant to be names of people who take turns doing the thing.  Can specify multiple times as in the example above.
 - ***title***: the thing to be done.  If not specified, defaults to just "turn".

## Deployment

Meant to be used with the Flash Briefing [blueprint](https://blueprints.amazon.com), as described in this [blog post](https://blog.garble.org/).

When you deploy, be sure to deploy as a web app and make it available to anyone.
