---
layout: post
title:  "The WhisperFrame Generates Art From Conversations"
date:   2023-09-17 23:55:45 +0000
tags: maker projects youtube ai
---

# The WhisperFrame

The WhisperFrame listens to conversations in our living room and then generates art based on those conversations. It's a pretty simple concept:

1. Record snippets of the conversations
2. Convert those to text via OpenAI's Whisper API
3. Combine recent transcripts together and have GPT-4 pick a topic and generate an image prompt
5. Use Stable Diffusion to generate an image from the prompt
6. Show it in the living room!

Ours generates a new image after every 5 minutes of active conversation. When there hasn't been any talking, it will revert to showing randomly selected images generated in the past.

<iframe width="560" height="315" src="https://www.youtube.com/embed/PCUJBcXRGKw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Check out the images and prompts (658 of them) it has generated from our <a href="https://whisperframe.morehavoc.com" target="_blank">living room</a>.

It was a fun project; I even created a second one for my office that generates images during meetings! It might even be a new way to make meeting notes, a list of images representing the meeting instead of action items. It probably won't catch on, though!