---
layout: blog
title: Diving deeper into "meshaging"
categories: messaging,chat,UX,applications
created: 2012-10-08
changed: 2012-10-29
post_author: The Work Department
lang: en
---
  <p>In our recent <a href="https://commotionwireless.net/blog/exploring-meshaging" target="_blank">blog post about messaging</a>, we introduced our &ldquo;meshaging&rdquo; (basic chat) application and explained some of the plans for our future work with it. We are still working on this project and have diagrammed how exactly communication happens in the application. This has improved our internal process and we think it&#39;s beneficial to share.</p>
<p>Compared to centralized, server-based systems, decentralized networking applications are a bit messy: with the benefit of decentralization comes the cost of increased complexity. Maintaining consistency of data across a mesh network is a hard problem to solve, and there are plenty of interesting approaches to address this problem. As designers, we became interested in embracing inconsistency: what systems could exist, or even thrive, in a network of inconsistent connections or transient devices? This is important to consider because a mesh network could be constantly changing.</p>