---
title: Marked 2 and Obsidian
created: 2025-04-28T10:04:41 (UTC +02:00)
tags: [wiki links]
source: https://brettterpstra.com/2024/05/16/marked-2-and-obsidian/
---

# Marked 2 and Obsidian - BrettTerpstra.com

> ## Excerpt
> I’m not going to lie, Obsidian is really cool. It’s a Markdown-based note system that has a ton of cool features, and even more with its healthy plugin community.

![Obsidian and Marked 2 icons](https://cdn3.brettterpstra.com/uploads/2024/04/obsidian-marked-rb.jpg "Obsidian and Marked 2 icons")

I’m not going to lie, [Obsidian](https://obsidian.md/ "Obsidian-Sharpen your thinking") is really cool. It’s a Markdown-based note system that has a ton of cool features, and even more with its healthy plugin community.

I don’t see Obsidian as direct competition for [nvUltra](https://nvultra.com/ "nvUltra-Searchable, portable, MultiMarkdown notes")[](https://brettterpstra.com/2024/05/16/marked-2-and-obsidian/#), where the main focus is rapid note-taking and full text search, which nvUltra does a superior job of. I actually open my main nvUltra Notebook in Obsidian as a Vault (both of which are just folders on your drive) and love the ease of using both apps together.

Lee Garrett and Mike Schmitz have done some great Obsidian tutorials over at [ScreenCastsOnline](https://screencastsonline.com/members/aff/go/bterpstra). Check out:

-   [Obsidian Basics](https://www.screencastsonline.com/tutorials/productivity/obsidian-basics?ref=bterpstra) from Lee, giving a full tutorial for getting started with Obsidian
-   [Obsidian Plugins Starter Kit](https://www.screencastsonline.com/tutorials/productivity/obsidian-plugins-starter-kit?ref=bterpstra) from Mike, offering an overview of some great core and community plugins, with tips that will also serve you well for getting used to using plugins in general

(I have an affiliate arrangement with SCO that gives me a little income if you subscribe. They make amazing videos so I’m very happy to partner with them!)

### Integrating with Marked 2

The point of this post is not to get you to use Obsidian. It’s about integrating [Marked 2](https://marked2app.com/ "Smarter tools for smarter writers") with Obsidian for those who already use it. Obsidian plugins offer some great Markdown preview features, but lack all of the writing and customization tools that Marked offers.

Marked works perfectly with Obsidian. You just have to open the current note in Marked and changes show up with about a two-second delay in Marked as you edit (based on the rate that Obsidian autosaves). You can also open your entire Vault folder in Marked and it will always show you the note you’re currently editing. It’s just a bit of a pain to get these to Marked without revealing in Finder and dragging. So I made [a plugin](https://github.com/ttscoff/Marked2-obsidian "ttscoff/Marked2-obsidian").

![marked-sidebar-2.jpg](https://cdn3.brettterpstra.com/uploads/2024/04/marked-sidebar-2.jpg "marked-sidebar-2.jpg")

Eventually I’d like to have this plugin available in Obsidian’s Community Plugins, but the process of getting it accepted has been slow. If and when it is eventually merged, I’ll update these instructions as the process will become much easier. In the meantime, you have two options to install:

#### Use the B.R.A.T. Plugin

Install [the BRAT plugin](https://github.com/TfTHacker/obsidian42-brat). Then add the Marked 2 plugin repo URL:

```
https://github.com/ttscoff/Marked2-obsidian
```

Copy

(Thanks to [Mason Phillips](https://mastodon.social/@phillipsmn) for pointing this option out.)

#### Install Manually

1.  Open the `.obsidian/plugins` folder in your Vault. The easiest way to get there is to open Obsidian Preferences, navigate to Community Plugins, then click the folder icon next to Installed Plugins.
    
![browse-obsidian-plugins-800.jpg](https://cdn3.brettterpstra.com/uploads/2024/05/browse-obsidian-plugins-800.jpg "browse-obsidian-plugins-800.jpg")
2.  Create a folder called `Marked-obsidian` in the plugins folder.
3.  Go to [the latest release](https://github.com/ttscoff/Marked2-obsidian/releases/latest) of the Marked 2 plugin and download the `main.js` and `manifest.json` files to the `.obsidian/plugins/Marked-obsidian` folder.
4.  Return to Obsidian Preferences -> Community Plugins and you should now see the Marked plugin available. Enable it by clicking the slider.

This gives you a sidebar button for opening the current note in Marked (which can be “Marked blue” or neutral to fit your theme), as well as two commands in the palette: “Open note in Marked” and “Open vault in Marked.”

![obsidian-commands-800.jpg](https://cdn3.brettterpstra.com/uploads/2024/04/obsidian-commands-800.jpg "obsidian-commands-800.jpg")

### Handling Obsidian Syntax

If you’re regularly opening Obsidian files in Marked, you might want to add a Custom Preprocessor for handling general Obsidian markup:

1.  There’s [this one](https://github.com/voostindie/obsidian-md-filter) from voostinidie that does things like stripping YAML, stripping emojis, and converting wiki links to plain text. It has the nice benefit of replacing `![[file include]]` syntax with IA block syntax, which Marked will render. I may eventually add the Obsidian formatting as a valid option for file includes in Marked by default, based on interest. I had a PR accepted to this repo that adds some additional config options for replacing `[[wiki links]]` and other Obsidian syntax with links back to the note/header in Obsidian. See the README for configuration details. [My own fork](https://github.com/ttscoff/obsidian-md-filter) will always have the latest changes.
2.  This [much simpler one](https://gist.github.com/radekkozak/9b07af0ff3c90d4dc51d3a4ab41b5b8f?permalink_comment_id=3740329) from radekkozak just handles wiki links, and converts them to `obsidian://` links for you, so clicking a link in Marked will open the linked note in Obsidian.

> If you want to be able to render Obsidian notes differently from your usual documents in Marked, [Conductor](https://brettterpstra.com/projects/conductor/ "Introducing the Marked Conductor") is the perfect solution. You can see my own rules for handling Obsidian notes in the [sample config](https://github.com/ttscoff/conductor-config/) I provide.

This is my first Obsidian plugin, and I’m not a regular Obsidian user (yet), so I don’t know if I’m going to really dig into creating more in the future. But this one serves its purpose well and I think a lot of people will find it handy.

By the way, one handy feature of Obsidian is [Obsidian Sync](https://obsidian.md/sync), which is a paid add-on. But never fear, there’s a giveaway coming up [later this year](https://brettterpstra.com/giveaways/upcoming/) that will get you a free year. [Sign up for the newsletter](https://brettterpstra.com/subscribe/) to stay in the loop on all of the sweet giveaways I have lined up.
[Marked 2 and Obsidian - BrettTerpstra.com](https://brettterpstra.com/2024/05/16/marked-2-and-obsidian/)

[appunto](/%2F/appunto.md)
