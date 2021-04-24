# It’s a glorious day when Apple fixes your bug
It takes a minor miracle to get Apple to fix a bug in any of its software or services. Just look at all the discussion threads on their forum.

The thing that’s been killing me for months? **Dumb Smart Reminders.** Apple claimed that, in iOS 9 and OS X El Capitan, you’d be able to remind yourself about virtually anything on your device - a note, a text message, a Trello card, a file on your FTP server - and the reminder would be saved with a simple contextual link for quick access.

Problem is, it’s been categorically broken. Ironically enough, it’s broken when you try to use your phone in the way Apple keeps pushing us to use it - through Siri’s (admittedly mostly great) voice recognition. 

If you wanted to remind yourself about a website you were viewing on your phone, and you decided to use Siri to do that, Reminders would (sometimes) create a link correctly to Safari. If you happened to have another app installed on your phone at all (in my case, Ticketmaster, Google Chrome and TripAdvisor), Reminders would *instead* link to one of those apps - then if I tried to access the website, iOS would attempt to open Ticketmaster and fail to render the website.

Argh.

It wouldn’t have been as infuriating if this was only an issue on iOS - but of course it happened in OS X too. If I saved the same website to Reminders on my Mac using Safari, for some reason, Reminders would instead create a link to Chrome. This wasn’t **as** bad - at least the site would load - but when you’re like me and strictly use your web browsers for specific reasons (eg. Safari for personal, Chrome for work), this gets annoying.

The worst part, though, was that I could totally see what was happening: if I uninstalled TripAdvisor from my iPhone, Reminders would stop linking to it - but instead link to Ticketmaster. Then it’d link to Chrome if I uninstalled Ticketmaster. If I reinstalled TripAdvisor, it’d start linking there again. Basically, Reminders would work without any other apps potentially risking the link to Safari. You’d think that Apple coded this such that Reminders was aware of the source app of the Reminder, and persisted that link forever. There was some dumb app prioritization happening that was causing TripAdvisor to take preference over Ticketmaster, which got preference over Chrome, which got preference over Safari. *(No offense to any of these apps, they’re all great - which is why I have them on my phone, god damnit.)*

So, while I wanted to use Reminders for **exactly what Apple intended it for**, I couldn’t, and had to rely on another (admittedly great, but not for me) [app, 2Do, to manage my tasks][1].

---- 
Six days ago [Apple released the sixth *(sixth!)* public beta][2] of iOS 9.3. Yesterday morning, I got frustrated because I was duplicating task lists for my upcoming wedding in both Trello and 2Do - so I decided to try out Reminders again. Saving Trello cards as a Reminder seemed to work. Saving a Note seemed to work. Reminding myself about something in my Amazon wish list worked. Even a stupid webpage someone had sent me went correctly into a Reminders list.

Yesterday was a glorious day.

[1]:	http://2doapp.com
[2]:	http://www.macrumors.com/2016/03/07/apple-seeds-ios-9-3-beta-6/