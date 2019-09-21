# Nintex DocuSign Live Actions, Nothing Happening

More specifically this is the DocuSign action to send a document with content that is being generated on the fly.

Basically I found that there is a requirement that doesn't seem to be documented anywhere but that requirement is that the SharePoint farm
needs to have **Word Automation Services** setup and configured.

In hindsight this makes perfect sense as there has to be something generating the document that is being sent to then ultimately be signed.

I have come to this conclusion after having sat watching many a workflow be kicked off and just stuck in progress and nothing doing in the
logs.

I also kind of proved that there was not a deeper underlying issue by chosing to perform the same action but against a document that did
already exist in a document library.

So in a nutshell it is my belief that to choose the generate content on the fly option, **Word Automation** is required.
