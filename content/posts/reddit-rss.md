---
date: 2021-10-16T08:00:00+06:00
title: Reddit RSS Feeds limit
authors: ["flinner"]
weight: -230
---
# What are RSS feeds and why you need them
You don't know? Seriously? How did you end up here? :)

# How to get your RSS feed
To get straight to the point, just add `.rss` to the end of almost any reddit URL. Comments, Posts, Links, etc.

Example:
```
https://www.reddit.com/r/announcements.rss
```
That is it!

# My Feed reader is rejecting reddit urls!
Use `old.reddit.com`
```
https://old.reddit.com/r/announcements.rss
```
# RSS feed is spammy!
Ye what did you expect? ;)

You can sort by Top, New, Hot, Rising, or Controversial, and **then** add `.rss` to the end of the URL!

Example:
```
https://www.reddit.com/r/announcements/top.rss
```

In case you want to also filter by time, (example: top of this week), add `.rss` **before** the filter.

Example:
```
https://www.reddit.com/r/announcements/top/.rss?t=week
```

# Dude, even top of the week is A LOT! How do I get the top 25 posts?
Here is where the limit query comes into play, you can add a limit query as so `limit=25`. Take a note how two queries are separted by an ampersand, `&`. (in this case, two queries are `t=week` and `limit=25`)

Example:
```
https://www.reddit.com/r/announcements/top/.rss?t=week&limit=25
```

# I want **search** results, not just subreddits
Yeah just do the same with normal subreddit urls, do the search and add `.rss` at the end. (not really at then, add it before the `?`!)

Example:
```
https://www.reddit.com/search.rss?q=cats&sort=new&restrict_sr=&t=all
```

