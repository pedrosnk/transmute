---
layout: post
title:  "Welcome to Jekyll!"
date:   2023-08-28 11:36:07 -0400
categories: Jekyll
---

So this is a test I'm gonna run by using Jekyll as a replacemente for my personal website.
intersting thing I just noticed was that, it is actually very simple implementation. And that
we do have support for some liquid and code. For instance, the text below is generated via a
liquid code.

{{ 'hello' | capitalize | append: ' world.' }}

```liquid
  { { 'hello' | capitalize | append: ' world' }}
```

Having liquid language available on the tool is good but liquid itself is not great for complex
stuff. So, I believe that, most of the stuff done here can also come from a JS library.

Posts should stay on the `_posts` directory and they all should be writen on Markdown.
A new post can be created by just creating hte post with the proper metatag on the head of the file.

the support for code snipets is also neat. But it seems like this support comes mostly from the theme
itself and not from the tool.


```elixir
defmodule Fibonacci do
  def perform(num, acc = 1)

  def perform(0, acc), do: acc

  def perform(num, acc), do: perform(num - 1, acc * num)
end
```

To better evaluate it, I'm gonna create a list of things I want to achieve and later check it out
how far I could go.

- [ ] Generate a GH Page and host it
- [ ] Host it in my own cloud (nginx)
- [ ] Create a landing page with the introduction of myself
- [ ] Create a Resume page
- [ ] Write my own theme
- [ ] Write my own plugin
- [ ] Ramdomly blog on it every single day

So here I go, let's get started.
