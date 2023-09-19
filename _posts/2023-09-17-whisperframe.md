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

In general, the moving parts are:
1. A loop that records 15-20 seconds of audio, then sends it to the OpenAI Whisper API to get a transcript. And repeat. Every 5 minutes or so of recorded material, go to the next step.
2. Take the transcript and use GPT-4 to extract a topic as an image prompt. We manually created some outputs to give it a couple of examples to go by.
3. Send that prompt to Stable Diffusion to get an image. When done, return to step 1.

A separate Flask server runs in the background, serving up the current image, and every 5 minutes, checks again to see if there is a new image. If there hasn't been a new image in 30 minutes, it reverts to just showing random pictures from the list until a new one is generated.

This helps keep the content fresh and relevant to the conversation in the room.

It's a bit self-fulfilling in that as people talk about the image it drew, it becomes more likely that it tries to illustrate that one again, as the topic is more likely to be selected by GPT-4. But it's still awesome!

It was a fun project; I even created a second one for my office that generates images during meetings! It might even be a new way to make meeting notes, a list of images representing the meeting instead of action items. It probably won't catch on, though!