---
layout: post
title: "An Iconic Oak Engraved Into Wood"
description: "This laser engraving project involved taking an image of Tulane's 'Tree of Knowledge' and transforming it into a piece to be displayed at home."
tags: [laser engraving, Tulane, trees]
---

Here are some examples of what a post with images might look like. If you want to display two or three images next to each other responsively use `figure` with the appropriate `class`. Each instance of `figure` is auto-numbered and displayed in the caption.

## Figures (for images or video)

{% capture images %}
	/images/newOrleans3.jpg
	/images/tree.png
{% endcapture %}
{% include gallery images=images caption="Tree image transormed into a bitmap for rastering." cols=3 %}
