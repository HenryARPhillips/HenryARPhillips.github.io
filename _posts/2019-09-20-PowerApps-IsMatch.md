---
layout: default
title: PowerApps IsMatch Changes in behaviour
---

<h1>PowerApps IsMatch Changes in behaviour</h1>

Just a quick one to say that I found a few broken formulas today.

Previously working formula: **IsMatch(DataCardValue27.Text,Email)**

Changed to: **IsMatch(DataCardValue27.Text,Match.Email)**

So I do have a theory that it could have been the way I named another control within the app as it basically seemed to be looking to Email as a control, rather than a match.

So this is just a good way to remind you that if you explicitly define it is the Email relating to a match by way of Match.Email or Match.* for other match formats, then it can
get you past the type of issue I faced today or if you do it in the first place it could avoid something breaking further down the line.
