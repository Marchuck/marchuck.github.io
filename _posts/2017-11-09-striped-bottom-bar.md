---
layout: post
title: "Android BottomBar with stripes"
date: 2017-11-09
---

Well. Recently I was asked to design bottom navigation on Android. However it smells like iOS pattern, and most of my colleagues are more likely to NOT follow iOS principles, I hadn't had conscience.
I quickly found cool library for my use-case

[BottomBar](https://github.com/roughike/BottomBar)

I faced a few obstacles during development, but learned how library works underneath. One of the most curious part was parsing the tabs defined at `(res/xml/bottombar_tabs.xml)` where I was able to define stripeColor:

```
<?xml version="1.0" encoding="utf-8"?>
<tabs>
    <tab
        stripeColor="#7c4dff"
        icon="@drawable/ic_recents"
        id="@+id/tab_recents"
        title="Recents"/>
    <tab
        stripeColor="#e53935"
        icon="@drawable/ic_favorites"
        id="@+id/tab_favorites"
        title="Favorites"/>
        ...
```

Bonus: I've added custom callback in order to customize `BottomBar` stripe enter and exit animation.
See [StripedTabsActivity](https://github.com/Marchuck/BottomBar/blob/feature/striped_tabs/app/src/main/java/com/example/bottombar/sample/StripedTabsActivity.java) to see this customization in action!



[Here's the result](https://github.com/Marchuck/marchuck.github.io/blob/master/assets/nov/bottom_bar_stripes.gif)


Do you like this? Don't forget to star or fork :)

Check out `feature/striped_tabs` branch [here](https://github.com/Marchuck/BottomBar)
