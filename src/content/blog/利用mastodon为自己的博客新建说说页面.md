---
pubDate: "2023-12-28T07:22:00Z"
title: "利用mastodon为自己的博客新建说说页面"
keywords:
  - 分享
tags:
  - mastodon
description: "本文介绍了如何利用Mastodon为自己的博客新建说说页面。通过复制粘贴代码并更改实例地址和user id，可以创建一个包含Mastodon时间线的页面。文章还提供了设置步骤和获取user id的方法，并给出了一个演示地址供参考。"
draft: "false"
---

## 项目

https://gitlab.com/idotj/mastodon-embed-feed-timeline

**GoToSocial与mastodon适用**

## 实现步骤

新建页面把以下代码复制粘贴,更改其中的实例地址和user id即可
 
## 设置

如何设置

### 获取user\_id的方法

 右键点击自己的头像,新标签页打开 获得头像地址为 https://im.loliko.cn/accounts/avatars/111/363/033/003/475/492/original/f726dbce158df8b9.jpg 从avatars/之后/original之前的一串数字111/363/033/003/475/492/去掉所有的/得到\*\*111363033003475492\*\*即是 `user_id` \

### 参数
 
```
  // 默认: "https://mastodon.social"
  instanceUrl: "实例地址",

  // 可选模式: 'local', 'profile', 'hashtag' 默认为'local'
  timelineType: "local",

  // 你的用户ID,默认为空
  userId: "",

  // 你在实例中的用户名以` @ `开头
  // 如果你没有选择 'profile' 作为时间轴,则留空,默认留空
  profileName: "",

  // 标签名称 (不包含`#`符号) 如果不选择 `hashtag` 模式则留空,默认为空
  hashtagName: "",
 

  // 可选风格样式: "light", "dark" or "auto" 默认为: "auto"
  defaultTheme: "auto",

  // 请求的帖子数量,默认: "20"
  maxNbPostFetch: "20",

  // 在时间轴显示最大的帖子数量,默认 : "20"
  maxNbPostShow: "20",
 

  // 隐藏未列出的帖子 (默认:不隐藏)
  hideUnlisted: false,

  // Hide boosted posts
  // Default: false (don't hide)
  hideReblog: false,

  // 隐藏回复的内容 (默认:不隐藏)
  hideReplies: false,

  // Hide pinned posts from the profile timeline
  // Default: false (don't hide)
  hidePinnedPosts: false,

  // 隐藏用户名下的用户账号 (默认 : 不隐藏)
  hideUserAccount: false,

  // Limit the text content to a maximum number of lines
  // Use "0" to show no text
  // Default: "" (unlimited)
  txtMaxLines: "",

  // Customize the text of the button used for showing/hiding sensitive/spoiler text
  btnShowMore: "SHOW MORE",
  btnShowLess: "SHOW LESS",  

  // Converts Markdown symbol ">" at the beginning of a paragraph into a blockquote HTML tag
  // Default: false (don't apply)
  markdownBlockquote: false,  

  // Hide custom emojis available on the server
  // Default: false (don't hide)
  hideEmojos: false,  

  // Customize the text of the button used for showing a sensitive/spoiler media content
  btnShowContent: "SHOW CONTENT",  

  // Hide video image preview and load the video player instead
  // Default: false (don't hide)
  hideVideoPreview: false,

  // Customize the text of the button used for the image preview to play the video
  btnPlayVideoTxt: "Load and play video",  

  // Hide preview card if post contains a link, photo or video from a Url
  // Default: false (don't hide)
  hidePreviewLink: false,

  // Limit the preview text description to a maximum number of lines
  // Use "0" to show no text
  // Default: "" (unlimited)
  previewMaxLines: "",

  // Hide replies, boosts and favourites posts counter
  // Default: false (don't hide)
  hideCounterBar: false,

  // Disable a carousel/lightbox when the user clicks on a picture in a post
  // Default: false (not disabled)
  disableCarousel: false,

  // Customize the text of the buttons used for the carousel/lightbox
  carouselCloseTxt: "Close carousel",
  carouselPrevTxt: "Previous media item",
  carouselNextTxt: "Next media item", 

  // Customize the text of the button pointing to the Mastodon page placed at the end of the timeline
  // Leave the value empty to hide it
  btnSeeMore: "See more posts at Mastodon",

  // Customize the text of the button reloading the list of posts placed at the end of the timeline
  // Leave the value empty to hide it
  btnReload: "Refresh",

  // Keep searching for the main <div> container before building the timeline. Useful in some cases where extra time is needed to render the page
  // Default: false (don't apply)
  insistSearchContainer: false,

  // Defines the maximum time to continue searching for the main <div> container
  // Default: "3000" (3 seconds)
  insistSearchContainerTime: "3000",
```

## 演示地址

https://www.imsun.org/mastodon