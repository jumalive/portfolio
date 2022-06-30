**Frequent Asked Questions (FAQ)**

Find below the answers to some common questions about integrating Rich Presence with your game.

If you miss some question here, reach out to gamedevs@discord.com. 🙂

---
**Why do I see _"Playing MyGame"_, but no Rich Presence data?**

That might be because you are running two instances of the Discord client, or because your Discord_Initialize() function is incorrect. Throughout development, make sure you have your errored() and disconnected() callbacks hooked up for debugging. You can open up the console in Discord and look for errors pertaining to SET_ACTIVITY for more information as well.

---
**Why am I not seeing Spectate buttons on my profile?**

Make sure you applied for approval! If you want the Spectate button on your players' profiles, we require your integration to go through an approval process. If you have applied and have been approved and still don't see the buttons, check your Discord console for errors.

---
**What happens if someone has more than one game running that supports Rich Presence?**

The application that connected first is displayed. Due to recent changes in our infrastructure for support of multi-activities, the behavior of multiple connected Rich Presence apps has changed from what it was before. Previously, whichever application was focused would be the presence that was shown.

However, invite functionality across multiple connected applications now works no matter which app is display on a user's profile. For example, if you are hosting a Spotify listening party, playing Game A that allows you to send Join invites, and playing Game B that allows you to send Spectate invites, you'll be able to send invites to all three simultaneously!

---
**What if someone looking at my profile or an invite doesn't own the game?**

Anyone can see your profile data, whether they own the game or not. They'll only be able to interact with chat invites or profile buttons if they own the game and have launched it at least once. Otherwise, the invite/button tooltip will show "Game Not Detected".

---
**Do join invitations allow players to select the number of open slots?**

Currently, the SDK does not support this. Party slot information is determined by the party data you sent in your presence payload.

---
**Can I send images via the payload rather than uploading them to my Developer Dashboard?**

Yes! In addition to uploading an asset and specifying its name, you can also specify an external image URL for us to proxy. For more information, see Activity Asset Image.

---
**Can I change something in the SDK for my own purposes?**

Go nuts! The SDK is open source by design. If you need or want to change something for the purposes of your specific integration—like changing our JSON parser, or changing all of the variable names to the names of your pets—go ahead and tinker to your heart's content.

---
**OK—I've got it working! Now, how do I make my integration look awesome?**

I'm happy we preempted your question you asked! Check out our Rich Presence Best Practices guide for a rundown on how to make your integration the best that it can be!
