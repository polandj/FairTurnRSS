# FairTurnRSS

An RSS feed to power an Alexa skill for taking fair turns.  Supports the set of people to 
choose from and the name of the "thing" to do as GET parameters.

```
curl -L "https://script.google.com/macros/s/AKfycbxqq4TmQNyWZvekMwL4dOMZDWOYgxj3SJFLx1_8MJ6mBhIlWyWRUY2I-O982mMFnwR6tg/exec?option=KidOne&option=KidTwo&option=KidThree&title=turn%20to%20feed%20the%20dog"

```
Response
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

Meant to be used with the Flash Briefing blueprint.
