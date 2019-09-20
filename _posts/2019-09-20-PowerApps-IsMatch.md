---
layout: default
title: PowerApps IsMatch Changes in behaviour
---

<h1>PowerApps IsMatch Changes in behaviour<h1>

Just a quick one to say that I found a few broken formulas today.

Previously working formula: <em>IsMatch(DataCardValue27.Text,Email)<em>

Changed to: <em>IsMatch(DataCardValue27.Text,Match.Email)<em>

So I do have a theory that it could have been the way I named another control within the app as it basically seemed to be looking to Email, rather than as a match type but as a control within the app.
So this is just a good way to remind you that if you explicitly define it is the Email relating to a match by way of Match.Email or Match.* then it can
get you past the type of issue I faced today.
