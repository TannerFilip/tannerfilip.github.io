---
title: "The Status of Discourse"
tags: "Mozilla,Discourse"
date: "2014-02-08"
---

Discourse is something that Mozillians have been asking for for a while. For those unfamiliar with it, [Discourse](http://www.discourse.org) is something like forums combined with mailing lists. I’ve been fortunate enough to work with [Mozilla Community I.T.](https://wiki.mozilla.org/IT/Community) in this project. 

### Background 

We started back in early September 2013, planning to install and configure Discourse with Puppet.

Discourse was to be hosted on HP Cloud, using EnterpriseDB for PostgreSQL hosting. HP Cloud stopped offering EnterpriseDB in late 2013, leaving us to set up our own Postgres cluster, something none of us had done before.

We ultimately decided against using Puppet to install, and decided to give Docker a try. That didn’t quite work out either, and we had concerns with how we would update it, and the general security of using containers like Docker. About a week ago we decided against using either Docker or Puppet to install, and doing this either with a Bash script, or just manually.

### Latest Status

As of right now, we plan on using Amazon’s AWS to host Discourse, with the help of Mozilla Labs. We will be using EC2 in two locations for web servers, one in Ireland and one in Northern California. In front of these two servers will be an Elastic Load Balancer to balance the load between the two, as the name suggests. On the database side of things, we’ll use AWS’ RDS to host Postgres, and ElastiCache for Redis. Both Postgres and Redis will be in the Northern Calfornia area, as well. We’ll be taking advantage of Multi-AZ for Postgres, so if something were to happen in our availability zone, we’ll have a failback to reduce downtime.

If you’re a visual person like I am, here’s an ugly chart I made.

[Direct link](https://www.lucidchart.com/publicSegments/view/52f02453-e484-4591-91b0-2c230a004eaf/image.png)

### Looking Ahead 

I am anticipating for Discourse to be running, though not entirely customized, by a week from today, February 11\. I can’t predict any problems we’ll have installing it, we’ve done it time and time again on several different servers. Once we get our servers, we’ll be working hard to get Discourse to you.

Finally, I’d like to thank jp and Mozilla Labs for helping get us set up with AWS. This is a huge resource to us, and will be extremely helpful.

If you have any questions/comments/concerns/complaints, please get in touch with me. I’m in #communityit on IRC, or just comment here.
