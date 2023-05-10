---
layout: post
title:  "Using AI to Protect Web Form Inputs: Extending Beyond the Adopt-A-Drain Example"
date:   2023-05-10 12:30:45 +0000
tags: software ai
author: christopher moravec and GPT-4
---

> Note: This post is a brief summary of a video I made about using AI to keep names clean and safe in adopt-a-drain programs. I'll update this post when the video is available. This post was made by feeding the transcript of the video into GPT-4 and asking it to write a blog post. It was then edited by me.


Artificial Intelligence (AI) has become an integral part of our daily lives, from setting timers (via tools like Alexa) to writing code. One particular use of AI that I find interesting is its application in protecting web form inputs. In this blog post, we explore how GPT-4 AI can be used to safeguard input forms across various domains, using the "adopt-a-drain" program as just one example.

Web forms often require users to submit information, ranging from names and email addresses to more sensitive data such as credit card numbers. Ensuring that the submitted information is appropriate and valid is of utmost importance. For instance, in an Adopt-A-Drain program, users may submit creative names for drains that could be inappropriate or offensive. We can use GPT-4 to check those names when the user submits them.

GPT-4 AI can be used in chat mode to review the submitted inputs, regardless of the specific use case. By crafting a prompt that outlines the AI's role in assessing the appropriateness or validity of the submitted information, we can instruct the AI to provide feedback on whether the input passes or fails the required criteria. If the AI is uncertain, it can flag the input for review by a human moderator.

One of the significant advantages of using AI like GPT-4 is its ability to understand unstructured prompts. It can interpret instructions and provide responses in a conversational manner, making it easier to engage and interact with the AI. Furthermore, GPT-4 can be "programmed"<sup>1</sup> to respond in different tones, such as professional, funny, snarky, or sarcastic, depending on the desired outcome.

In addition to using GPT-4 AI, the OpenAI API offers a moderation endpoint, which acts as a first line of defense against inappropriate inputs. By categorizing the input, the moderation endpoint helps protect the system from offensive or invalid content. If the input passes the moderation endpoint, the more powerful GPT-4 AI can then be used to assess the input's suitability or validity.

In conclusion, AI like GPT-4 offers a powerful and adaptable solution to protect web form inputs across various domains. By crafting the right prompts and utilizing AI's conversational abilities, we can create systems that ensure appropriate and valid content is submitted. The Adopt-A-Drain example is just one instance demonstrating the potential of AI in safeguarding web form inputs, and its applications can be extended to numerous other scenarios.


### Footnotes
1 - I put programmed in quotes because you are really just telling it, like you would a human doing the same work.