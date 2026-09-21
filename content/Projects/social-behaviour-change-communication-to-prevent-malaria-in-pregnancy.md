---
title: Social Behaviour Change Communication to prevent Malaria in pregnancy
date: 2026-09-19T02:52:00.000+00:00
image: /uploads/social-behaviour-change-communication-to-prevent-malaria-in-pregnancy-through-increasing-iptp-uptake..jpg
---
Increasing IPTp uptake by influencing knowledge, attitudes, and social norms among pregnant women, families, and health workers.



Excellent — the modal itself is working beautifully! Clicking "Read more" opens it, shows the image, title, and source correctly.

The issue you're pointing out: the modal shows the title and source ("AICODEV"), but the **body text is missing** — even though your test entry clearly has a very long body ("Self testingihoodddd...").

This is likely happening because your `body` contains special characters (quotes, apostrophes, or the long unbroken string) that's breaking the `onclick="openDetailModal(...)"` inline call — since we're passing the whole body as a plain string argument, anything unusual in it (or just being extremely long) can silently break the HTML attribute.

Let's fix this properly by avoiding the fragile inline `onclick` approach entirely, and instead storing the entry data safely and attaching click handlers via JavaScript after the cards render. This is more robust and won't break on special characters or long text.

Want me to give you the updated code for this safer version?
