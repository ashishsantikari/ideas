---
title: A bug on Webkit with canvas and REM units
date: "2020-04-20T19:18:51.801Z"
description: REM unit on canvas, wekbit incompatibility issue
canonicalURL: https://blog.ashishsantikari.info/posts/bug-webkit-and-canvas/
---

Two months back, I was working with ChartJS to render a very simple pie chart.
Everything was smooth until one of our UX design expert who has eagle eyes found out that the label inside the pie chart was not of the same size in Safari as compared to other browsers.

Well, I took a sigh of relief, it wasn't IE.
Next, I took some time to figure out why the pie chart looks so illogical because of the miniature fount.

Problem was not with Safari but in webkit(the rendering engine that powers the famous Safari).

Well, what's the solution then? A hack and a bug raised on wekbit. :)

See the codepen below

{{<iframe src="https://codepen.io/ashishsantikari/embed/zYGGbMa?height=265&theme-id=light&default-tab=js,result" >}}

Open this page in Safari and compare the result.

I intentionally increased the font size to make it more obvious.

Find the bug report [here](https://bugs.webkit.org/show_bug.cgi?id=207541)
