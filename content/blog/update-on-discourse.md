---
title: "Update on Discourse"
tags: "Mozilla,Discourse"
date: "2014-02-14"
---

Earlier this week I wrote about the [status of Discourse](http://tannerfilip.org/post/the-status-of-discourse/) within the Mozilla community. The next day, we recieved access to Mozilla Labs’ AWS account, and almost immediately started setting Discourse up. We now have [Discourse running](https://discourse.mozilla-community.org/), so please feel free to use it! Occasionally signing doesn’t work the first time. Reload the page and try again if this happens. Jan Bambach is working to make Discourse fit Mozilla’s style, and the theme is shaping up really well. Huge thanks to him for doing this. There was one minor change with our infrastructure. Instead of placing a server in Ireland and Northern California, we put both webheads in Northern California, but in two different availability zones.

#### What we learned

[xkcd automation](http://imgs.xkcd.com/comics/automation.png)

Source: [xkcd](https://xkcd.com/1319/)

As I mentioned previously, we spent a lot of time trying to automate the installation of Discourse. This didn’t work out so well, and it was ultimately what stopped us from having Discourse running quite a while ago. Yousef and I spent maybe two hours manually installing Discourse on our two webheads, but much more time trying to configure Puppet and/or Docker to install it for us. I totally understand that these would be great if we had to deploy on dozens of servers, but it wasn’t worth our time to do it for just two. I will, though, say that I can’t wait until we have Puppet/Ansible/Chef/whatever working for configuration management. Even changing files on two servers can be tedious, so that should help speed things up for us.

#### Thanks!

I’d like to thank a few people for helping out with Discourse. In alphabetical order…

*   [Yousef Alam](http://yalam.co.uk)
*   [Jan Bambach](http://janbamba.ch)
*   [Will Dowling](https://discourse.mozilla-community.org/users/wdowling/)
*   [Tom Farrow](http://tomfarrow.info/)
*   [Logan Rosen](http://www.loganrosen.com/)
*   [JP Schneider](http://jdotp.org/)
*   [Matthew Zeier](http://mrz.velvet.org/)

#### Suggestions?

If you have any problems, suggestions, comments, etc. please let us know! We all hang out in #communityit on IRC, and I’ll make a category on Discourse for suggestions for Discourse. If you want to use Discourse for your community/project/team/etc, also let us know. We’ll have a Bugzilla form shortly to request these, but until we do, I can handle them.

Enjoy!
