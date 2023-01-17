---
layout: post
title:  "NFTs from a Camera!"
date:   2023-01-10 23:55:45 +0000
tags: ideas crypto maker nft
author: christopher moravec
---

# NFTs

I don't really want to cover what an NFT is here in this post, there are lots of places
to read about that, like here, or here, or here is a funny story about some NFTs...

What you need to know for this idea to make sense is that an NFT is a way to make a
digital thing unique. If you make a painting, there is only one original. If you take a
picture on film, that's your original. It's uniqueness gives it some of it's value.

With an NFT, you can make a digital asset unique. You can then sell it as though it was the only one.

# AI

One other thing... AI image tools have gotten pretty good and are only getting better. I can feed prompt like this into Dall-E:

```
a photograph of the Eiffel tower taken across the seine with the champ de mars in the background and a beautiful sunset behind it.
```

And get this, slightly impossible picture:

![OpenAI Dall-e generated photo of the Eiffel tower](/assets/images/2023-01-11-the-nft-camera-dalle.png)

<details>
<summary>Why can't this picture be real? (other than the obvious funny business?)</summary>
<p>
This should be taken from roughly the north side of the Eiffel tower, with a sunset to the south, which shouldn't be possible.
<img alt="Image that exmplains why this camera position can't be real" src="/assets/images/2023-01-11-the-nft-camera-camera-position.png">
</p>
</details>
<br/>

How do we know photographs are real? How do we know they were really taken by a human, and at the real place?

# NFTs direct from a Camera

The idea here is that you have a physical device that let's you take pictures. This device is not your phone, we'll call it
a [**Camera**](https://en.wikipedia.org/wiki/History_of_the_camera) for lack of a better word. When you take a picture with this device you can preview it, and if you approve it, and if the camera has a connection to the internet, it will:

1. Write it directly to [IPFS](https://en.wikipedia.org/wiki/InterPlanetary_File_System) and get it's global URI back
2. Write the global URI to the etherium ledger as belonging to the owner of the camera.

A few notes:
* The image is *never* written to disk anwyere, it it stored in RAM and then written directly to IPFS.
* The *original* image is copied. If you want to edit it, you can get it from IPFS and use it as you normally would.
* There could be a whole set of additions to photo editing software to handle the chain of changes for an image. As you work on it, the new one is written to IPFS and marked on the ledger as yours, and being relative to it's parent image. This keeps a chain of custody for the image as you touch it up.

# The project

It might be fun to build a simple version of this. Perhaps using a Circut Python board, a simple serial enabled camera and perhaps a nice case to put it all in.

It even would have the added benefit of being pretty low resolution, really bringing back that old digital camera feel! 

;-)