<b> PowerApp Instigated Flow not Executing or Missing Ask in PowerApps property in Flow Failure Details </b>

So really annoying one this as I know there are always issues when modifying a Flow bound to PowerApps, especially when you are changing ask in PowerApps
properties. But we usually combat this by removing and re-adding in PowerApps and potentially just placing "" where old references are still present to
allow the formula to be valid in PowerApps to allow for execution.

<b> Flow not Executing at ALL!!! (I am not mad, honest!) </b>

This turned out to be due to blank properties, you heard right it just flat out refused to run. No formula issue, no flow issue, just no blinking run!
I get that it is probably thinking well what is the point if I don't have the info but I would at least expect some sort of tap on the shoulder
or just a failed flow run will do. As in my situation I was collecting Signature images from a SharePoint library and I would still like the flow
to not kill the rest of the logic on the odd occassion there is no signature.

<b> Flow Fails Immediately </b>

So this was a by product of the first issue, in that I had a Flow run and grab signatures and then populate a variable with said signatures. This
was then in turn placed into some JSON to be passed to another Flow, so I could populate a template and have a finalised output thanks to the amazing
Plumsail actions.

So all I saw was a message stating that the compose_inputs property that it detected and was specified in PowerApps was missing. So I was messing around
for ages removing, re-adding, renaming the action and adding in another ask in powerapps property and then removing and re-adding and you get the picture.

It was when doing the removing and re-adding for the 100th time I placed "" in the property that was missing to place the actual JSON variable in the new property.
I then saw that the flow was no longer failing with a missing property on the new ask in PowerApps but the original one that it said was missing was now there.

<b> Lightbulb Moment! </b>

So I thought oh yeah!, hope is not lost. It is not the property but the property value, way to go PowerApps and Flow error handling shame on you.
Yeah yeah, I was trying to specify a blank value, that is me but I expected better from you.

So the JSON that was blank was due to the first flow not executing. I then tried to do a IsBlank do "" and if not do the actual signature but that still
didn't work, so in the end I settled on !IsBlank do the value, else carry on and that seemed fine.

<b> Key Takeaway </b>

<b> PROPERTY VALUE MISSING </b> not <b> PROPERTY NAME </b>





