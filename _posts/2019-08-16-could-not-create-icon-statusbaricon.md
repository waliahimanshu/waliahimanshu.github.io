---
layout: post
title: "Bad notification posted from package : Couldn't create icon: StatusBarIcon"
comments: true
author: "waliahimanshu"
meta: "android notification error"
categories: Android
---

<b>Exception</b>:
*android.app.RemoteServiceException: Bad notification posted from package : Couldn't create icon: StatusBarIcon*

### Fix
 *Use alpha only icon.*

### What are alpha only icons?
Alpha only icons are transparent icons, where 
_white acts as the visible area and black acts as the transparent area_.
For example, all [material icons](https://material.io/resources/icons/?style=baseline)
are alpha only.


### Reason
Since android L onwards :
>The system ignores all *non-alpha channels* in action icons and the main notification icon. 
You should assume that these icons are alpha-only.

So this exception occurs when colored image resource is used as a notification icon.

### Why can't use colored image resource ?
Device status bar backgrounds color could be of any color.
There are tons of manufactures and people apply themes etc.

So Android framework only allows alpha only icons as they will be visible on any colored status bar.


```java
 NotificationCompat.Builder(context, channelId)
 .setSmallIcon(R.drawable.ic_alpha_icon_for_notifications) //alpha only icon
 .setColor(ContextCompat.getColor(applicationContext, R.color.green)) 
 // adds your brand color over alpha icon
```

<hr>