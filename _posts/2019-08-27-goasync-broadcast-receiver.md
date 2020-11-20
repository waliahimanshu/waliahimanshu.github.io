---
layout: post
title: "Async work on BroadcastReceiver"
comments: true
author: "waliahimanshu"
meta: "android Async on BroadcastReceiver"
categories: Android
---

<b>Problem</b>:
I cannot perform any long running operation (aka IO operation) inside BroadcastReceiver as it dies immediately after receiving the intent.

{% include category_include.html %}


<b>Why</b>
`BroadcastReceiver.onReceive` always run in the UIthread (also main thread).
That means, you can not perform any long running operation.

However, in only rare cases when you need BroadcastReceiver to live longer, by using `goAsync()` we can tell the android framework to keep the receiver for longer approx `30` seconds.

```ruby
override fun onReceive(context: Context, intent: Intent?) {

        val pendingResult = goAsync()

        Thread(Runnable {
          val id = intent?.getStringExtra(ARG_ID_KEY)
            id?.let {
                // perform long operation task
           }

            //let the system know the BroadcastReceiver can now //finish
            pendingResult.finish() 

        }).start()
    }
```
<hr>



