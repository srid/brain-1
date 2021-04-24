# Running a dumb robot vacuum with Shortcuts
I love the idea of a totally self-sufficient robotic vacuum to keep my floors clean. However, I am also cheap: [a $1000 Roomba that empties its own waste][1] is amazing, but not something I’m willing to chalk up for at this point in my life.

So, I got an [Ecovacs Deebot N79][2] for sale on Amazon a few months ago. It’s great, but it’s also pretty dumb. Alicia and I call it DJ Roomba ([obviously][3]), and it’s very cute but kind of dumb.

It can schedule itself to run daily at a certain time, but no more granularly than that — I don’t want to hear a vacuum at 11am when I’m at home, but I do appreciate coming home to a clean house when I’m out and about. It does have Wifi capability and a companion iPhone app, but the app sucks: it requires 2 taps and several seconds of delay just to find DJ Roomba, and then I have to tell it what to do, and every time I want it to do something different I need to repeat this entire process.

It’s not great. I’d rather just build a scheme that DJ Roomba can follow automatically, whenever I want it to.


### Homebridge and its flaws
I naturally Google’d the crap out of this problem. I quickly found  **[sucks][4]**, a Python interface that connects to Ecovacs’ server and then enables one to issue commands to any robovacuums tied to your Ecovacs account. This was easy enough to set up. I then found a way to [connect `sucks` to Homebridge via a plugin called CmdSwitch2][5].

I had never used [Homebridge][6] before, but I love the potential of HomeKit. I already have a moderately robust HomeKit setup in my apartment: some smart bulbs, a couple of switches (including a critically placed one controlling my modem) and a HomePod to yell at, so installing Homebridge on my Mac seemed like a fun little project.

Turns out I suck at and don’t enjoy the command line. The process of setting up Homebridge, connecting all the dots between Python, `sucks`, `cmdswitch2` as a trigger that exists inside Homebridge’s config, and Homebridge itself, was a tedious process that quickly lost my interest. I kept having to kill and restart Homebridge to make sure everything was playing nice. I must have scanned the Homebridge QR code into my iPhone’s Home app twenty times to get it registered as an accessory. 

The other major challenge: I didn’t want my wife to have to deal with this either, but we share an iMac. She uses it regularly for work, and often has to kill processes in order for Adobe apps to run optimally, or restart the computer if things go wrong — which also killed my Homebridge server. I found some options to automatically restart the server, and I could have kept trying those things, but my fun little hobby project of _automating control of my dumb vacuum_ was increasingly frustrating me. I’d go to start the vacuum and constantly see the damn “No Response” in red.

So I gave up and dismantled the entire thing.

A few weeks later I realized that I don’t actually need Homebridge or `cmdswitch2` at all. I really just wanted to run `sucks` on command: ideally a specific times of day or when I’m home, but just being able to trigger it from any of my devices (or my voice) would suffice.

Enter crazy and powerful **Shortcuts**.

### Shortcuts and a simple AppleScript
Nobody I know personally really uses Shortcuts, but it’s sort of my lifeblood for controlling things around my home and work. I use it to set reminders without thinking, do a whole host of chores every morning & weekend, and generate canned email templates that I shouldn’t have to send as often as I do.

[Viticci][7] opened my eyes to the idea of [Shortcuts triggering actions on a remote Mac via SSH][8], including waking it from sleep. I figured out that I could also run AppleScripts using the an SSH command — `osascript`. 

I realize that most tech people probably know this already, but bear with me.

I then did the following:
1. On my shared iMac, opened up Script Editor and created an AppleScript (.scpt) file that run a basic `sucks` command: `sucks edge 15 clean 30 charge`. This script, when run, tells Ecovacs to run the “edge” function on my vacuum for 15 minutes, then general cleaning for a half hour, then send the vacuum back to its charger.
2. Saved that .scpt file my parent user directory on the iMac.
3. In Shortcuts, wrote a very simple (1-step) Shortcut that triggers script via SSH. Rather than SSH-ing into the iMac locally, I enable SSH access and file sharing on the iMac, then connect to its IP address so I can run the command from anywhere.
4. Repeated steps 1, but with a different script that simply tells DJ Roomba to go home, it’s drunk: `sucks charge`

Now I have two Shortcuts: Run Vacuum and Stop Vacuum. I can yell out to my HomePod, tap a button on my iPhone or iPad, to kick either process off. As long as my iMac is _on_, this will always work.

I can run this as part of another shortcut, such as my Bedtime Ritual one which darkens some lights around the home and reminds me to floss, clean out Roomba’s dustpan and a few other things. I can even have Reminders remind me to run the Run Vacuum shortcut at specific times or locations — for example, anytime I leave my house. Then, in one tap, DJ Roomba is up to his antics.

### The possibility in iOS 13
This works really nicely, but it’s not perfect. I’d love to customize even further when and how DJ Roomba can run. It sounds like this all gets unlocked in iOS 13 via Shortcuts Automations. I’ll be able to, for example, run the vacuum on Saturdays as long as nobody is home, something I can do currently but _only_ with HomeKit accessories.

This is really dumb and nerdy, but I find it satisfying and fun.

[1]:	https://www.amazon.com/iRobot-Automatic-Disposal-Connected-Edge-Sweeping/dp/B07NVTMJPD/ref=sxin_5_ac_d_rm?keywords=roomba&pd_rd_i=B07NVTMJPD&pd_rd_r=8e4c84bc-5f67-4929-af71-c3f4ee392806&pd_rd_w=cnQ5c&pd_rd_wg=i93iI&pf_rd_p=0bc35c17-1e0d-4808-b361-20ab11b00973&pf_rd_r=CA8HXGP9FD1CD2YMFHQT&qid=1560629136&s=gateway
[2]:	https://www.amazon.com/ECOVACS-Robotic-Cleaner-Low-pile-Connected/dp/B06XVXRYTM
[3]:	https://m.youtube.com/watch?v=pXhsUPtsiLU
[4]:	https://github.com/wpietri/sucks/blob/master/protocol.md
[5]:	https://www.reddit.com/r/homebridge/comments/8e1h7r/plugin_for_the_ecovacs_deebot_n79/
[6]:	https://github.com/nfarina/homebridge
[7]:	http://twitter.com/viticci
[8]:	https://www.macstories.net/shortcuts/#mac