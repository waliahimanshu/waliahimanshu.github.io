---
layout: post
title: "Android set multiple alarms using Alarm Manager"
comments: true
author: "waliahimanshu"
meta: "android notification error"
categories: Android
---

<b>Problem</b>:
I have scheduled multiple alarms using `Alarm  Manager`, but only one gets executed.


![image-title-here](/assets/arash-asghari-D58BEHSeX64-unsplash.jpg)


Other day, I was scheduling two alarms simultaneously, in future, but only one was triggering.

### When to use Alarm manger :

The Alarm Manager should be used for cases where you want to run your application code at a specific time in future, even if your application is not currently running.

In my case I had to trigger push notification after 2 and 4 hours in future, after a user has performed an action in the app.

When creating a pendingIntent that will perform a broadcast, 
we need to provide a unique request code param for the sender.

The problem was I was passing 0 as `requestCode` when creating pending intents for both alarms.

```ruby
Intent(appContext, AlarmReceiver::class.java).let { intent ->
            intent.putExtra(ARG_RECIPE_ID_KEY, recipeId)
            intent.putExtra(ARG_ALARM_TYPE, alarmType.name)
            PendingIntent.getBroadcast(appContext, 0, intent, 0)
        }

```

Solution:

I created a wrapper to be injected in a class from where I needed to set an alarm.

<script src="https://gist.github.com/waliahimanshu/c0d29361d1dad211fb17f72df1d48bad.js"></script>


Implementation :

<script src="https://gist.github.com/waliahimanshu/f927a9c1745bdd226320630d9fe996ee.js"></script>

Next, up perform long running IO tasks in reciver `onReceive` 

<hr>



