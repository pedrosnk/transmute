---
layout: post
title:  Creating a new Post on Jekyll
date:   2023-08-31 11:31:00 -0400
categories: Jekyll
published: true
---

## Introduction

This week I'm testing up using Jekyll for my daily use. right now
I'm just writting down on it the first impressions on creating
content and how it can be done. And it seems like out of the box
the only way to do it now is by creating a file by hand and just
write it down. This kinda bothers me, because I imagine all page
can have its particularity, and I honestly don't known how to
handle those particularities over all.

## The act of creating a new page

On Jekyl every makdown page is divided in two sections, the first
on the top is known as the Front Matter. adter the front-matter is
written down, there's the actuall content written in Markdown.

Front-matter is a YAML file included on the top of the markdown it is
used to address metadata to the page or post. This is actually pretty neat.
The metadata is visible first and later there's the content. the issue
I see is, we don't actually known what are the metadata that are supported
and which one I should worry about. Even wrost, ther's no command line
tool to help me quickstart a page.

I'm relying mostly on Jekyll page to look for documentation. And
what is wrost, is that some themes/layouts may require specific
metadata to be set on the page. And there's no linter or so to
help me understand which one should be used to achieve it.

## Looking for the layout page

While the initial theme (minima) is a nice quickstart, I'm stil confused
on how I can alter it down, it seems like I need to create a new theme
or a new layout to alter it down to add what need to be added.

Edit: I just found out that theres a Frotn-matter called `published`.
When it is set to false it hides the page for good. The first question I
have from that is, why this is not defaulted generated? Why those
neat options are hidden from everybody else?

## References

[Jekyll Post structure](https://jekyllrb.com/docs/posts/)
[Jekyll Front Matter](https://jekyllrb.com/docs/front-matter/)
