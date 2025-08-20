---
title: DRM free books
date: 2023-08-21T17:00:00
lastmod: 2024-02-08T11:02:00
images: 
- /img/drm-free-books/remove-drm.png
description: A guide on how to remove DRM from Kindle books and why I think it matters
tags: ['ebooks', 'guide', 'kindle']
---

{{< notice note >}}
From Feburary 26th 2025, Amazon has removed the 'Download and Transfer via USB' option so this guide no longer works
{{< /notice >}}

I really enjoy reading books on my Kindle. I also buy most of my digital books via Amazon. I never thought about making DRM-free copies of my eBooks until I read about how [an engineer had his Amazon account suspended](https://medium.com/@bjax_/a-tale-of-unwanted-disruption-my-week-without-amazon-df1074e3818b) due to a delivery driver's false claim.

That really got me thinking about how I would feel if I lost access to my Amazon account. I’ve purchased most of my ebooks from Amazon. Losing access would mean losing the majority of my digital library.

To avoid such a situation, I decided it was time to make a copy of the digital eBooks I purchased from Amazon.

This article covers how I removed the DRM from my Kindle ebooks so I can read my books on any device without needing to use a Kindle app.

Before going further, I’ll answer some questions some folks might have 👇🏽

## Quick Frequently Asked Questions (FAQ)

**What is DRM?**

DRM stands for Digital Rights Management. It’s a type of tech used to control and manage access to copyrighted content. Its main purpose is to prevent content from being shared with those that did not pay for it and to also prevent the content from being modified.

**What issues does it pose?**

While DRM is used to prevent piracy, it can cause issues for legitimate users as well.

For example, say you bought a video game that comes with some DRM that checks you own the game by contacting the game publisher’s server before you can play the game.

Now imagine if the game publisher went out of business and with that, the server used for the DRM check goes offline with it. Now you’re in a situation where you’ve paid for a video game but you can no longer access it due to the DRM server going offline (Also what if you just wanted to play the game offline/without an internet connection?).

Digital books from Amazon, are only intended to be read on Kindle devices and via the Kindle app using your Amazon account. If you lost access to your Amazon account for any reason, you would essentially lose access to the books you bought.

**Why should you care about removing DRM from your eBooks?**

That’s simple. Not having DRM on your eBooks means you can read them on any device using any app you want without having to worry about losing access to your books.

**Is it illegal to remove DRM from your digital items?**

No. Just don’t distribute the DRM-free books you have as that would be illegal.

{{< notice note >}}
There a several guides online that explain how to do this, I initially followed those methods but I got some errors when following these guides.

Below I’ve listed the steps that worked for me. You might find that this exact approach might not work for you.
{{< /notice >}}

### Prerequisites
You’ll need a Kindle eReader or the Kindle app on your machine. I personally used my Kindle eReader for this process.

Note - I use MacOS so these steps will be MacOS specific but the steps are similar if you are using a different operating system.

### Steps

1. First download [Calibre](https://calibre-ebook.com). It’s a free open source e-book manager.
2. Once you have Calibre installed, you’ll need to download the [NoDRM plugin](https://github.com/noDRM/DeDRM_tools/releases). 
3. Open the settings/preferences menu within Calibre and then click plug-ins under ‘Advanced’
4. Click the ‘Load plug-in from file’ option and then select the noDRM zip file you downloaded
5. Get your Kindle’s serial number from your Kindle device. You can find it under Settings > Device options > Device info
6. Go back to the plug-in menu in Calibre, select the NoDRM plug-in (under the file type sub-heading) and click ‘Customise plug-in’
7. Select ‘Kindle eInk ebooks’, click the green plus icon and enter your Kindle serial number and then click ok
8. Go back to the plug-ins menu, click ‘Get new plug-ins’ and then install the ‘KFX Input’ plug-in
9. Go to the Amazon website and then select the ‘Manage Your Content and Devices’ under your account menu and then click ‘Books’
10. Find the eBook you want to download and then select more actions > download and transfer via USB to download the eBook (Note - the file extension should be ‘AZW3’. I wasn’t able to get the ‘AFX’ file extension decryption/DRM removal working)
11. Drag and drop the eBook into the Calibre and then select ‘Convert Book” and then convert the book into whatever format you like (I usually go with ePub) and your eBook should have the DRM removed from it now 🎉

## What’s next?
Now that you’re able to remove DRM from your Kindle books you can read them on any device you like! If you want a Kindle like e-reader without having to buy a Kindle, you might want to consider a [Pocketbook](https://pocketbook.ch/en-ch) instead. 

### Where to buy eBooks going forward
You can of course still buy your eBooks from Amazon, but it might be worth exploring what other options exist that allow you to get DRM free books way more easily. One of my favourites is a website called [Hive](https://www.hive.co.uk/eBooks) which sells eBooks in ePub and PDF formats by default and most books are similarly priced to their Amazon counterparts.

That’s everything you should need to build a DRM-free digital library. All that’s left to do is to back up your eBooks somewhere (like a digital cloud provider) so you can always keep a copy of the books you bought).

*[Article header image by Vyshnav Gangadharan under CC 4.0 license](https://www.figma.com/community/file/1047875211730430527/Amazon-Kindle-Paperwhite-Mockup)*