# AndroidOSNotes
random notes on different technologies in Android


Adaptive Battery

best explaination:
https://www.youtube.com/watch?v=-7eZL3XRqas

Android in Marshmallow had two app states introduced with Doze: Active and Inactive.  Depending on your usage, apps will be put in one or the other buckets.  In Pie, Adaptive Battery extends this and uses 4 buckets: Active, Working Set, Frequent, Rare.  The adaptive battery machine learning algorithm buzzwordiness of it means it will try to move an app into active status if it learns to expect that you'll use an app w/in the next few hours.

What is restricted: jobs, alarms, services, cloud messaging, location updates, network-- and even when charging.

My notes:

You can force battery restrictions in an app's settings > battery screen.  Apps can also be restricted by excessive wakelocks.  Restricted state means it forgoes the learning and just calls it Rare (I guess).

To view or 'reset' the adaptive battery process, enable developer options and scroll down to Standby Apps.  Here you can see which state bucket each app is in.  If you wanted to 'reset' adaptive battery, I figure you could set all apps to a rare state, reboot your phone, and it will figure out which bucket apps need to be in again.

I also experiment with just going ahead and restricting all apps I know are not something I care about running all of the time when my eyes are not on the app: browsers, games, shopping apps, streaming video apps, etc.

What I wish they'd change: move this app state junk out of the Developer Options and into the Adaptive battery Screen.  Or have a little summary graphic to show how many apps are in each state.  The reason I think this is because the Adaptive Battery screen just looks useless.  One toggle and a pretty animation but I have no idea that it even does anything.  I also wish they would give me something that says "hey, we moved this app into this bucket and it reduced wakelocks by 4000 but you also didn't get 4 notifications on time."  I have no idea about the good or bad of adaptive battery.
