# iOS experiment: evaluating mixes
I haven’t written in a bit, but here’s some more stuff I’ve been thinking about in my spare time: listening to my music projects-in-progress in as many possible contexts as I can. 

Why is this more than a simple task? Audio files are big. Important: these are not your favorite streaming service’s audio files. These are hi-res, uncompressed, 24-to-32-bit audio files that are being semi-professionally mixed and mastered by a sound engineer for me. I can’t stream these without murdering my data plan, and there’s no easy or obvious way to put all these files I listen to within the stock iOS ecosystem. Plus, I need to manage and track changes to mixes easily as we address notes about those mixes. 

### issue 1: managing the recording project
I use [Trello][1] for all my recording projects currently, and their iOS apps are pretty fantastic and getting new and more complex features monthly. So no issues here. 

### issue 2: getting the mix
When James, my mixing/mastering engineer friend, has a mix for me, he usually posts a comment on Trello with the private S3 download link. I love how easy it is to just spin up a mix for listening, but this gets problematic when I'm on the go. I listen to a lot of music (including these mixes) on trains to and from work - streaming a 50-200 MB audio file is murder to my data plan, and way too slow for any meaningful listening. 

So I need to download to my phone as soon as I get James' mix. I've come to really appreciate **[Readdle Documents][2]** as my storage system for audio files, or any files, really. Documents has the ability to auto-sync any folder from any major cloud service. James (my mixing engineer) and I primarily rely on **Google Drive** and **Amazon S3** as our main repositories for managing and sharing files around our music projects; Google Drive’s got some nice revision history tracking that allow us to keep track of what’s changed in a particular file or session. I can dump any of James’ mixes into a Google Drive folder, and in less than 20 seconds, it’s on my phone ready for offline listening.

Amazon S3 is a different beast, though - we use it primarily for large session storage and archiving - but I still occasionally need to access that on the go. Panic’s excellent **[Transmit][3]** app makes browsing S3 buckets super easy, and it’s beautiful on my iPhone 6s Plus. Frankly, if Panic built Google Drive support and some local file sync support into the app, I’d probably use Transmit exclusively for all file management on iOS.

### issue 3: mix notes
As I mentioned above, we use Trello to manage the recording project at a high level. But sometimes I’ll be listening to a mix on the go and get a quick idea that I want to write down. Apple’s stock Notes app, with 3D Touch, makes for really quick note-taking that I can access later from anywhere. I love the new checklist feature in Apple Notes, mainly because it's nice to look at and super responsive. 

If you don’t have an iPhone with 3D Touch, [Drafts][4] is an excellent alternative here. It's super minimal and uses Markdown syntax to easily organize notes you take. You can even set up very custom share actions that allow you send your drafts anywhere in a swipe. 

In either case, I can easily take notes on the fly and share them to James in Trello or whichever messaging app in which we're talking. 

---- 
That's pretty much it. Not much to it, but I find it valuable to review how I perform more file-heavy, less-simple tasks with the constraints of iOS such that I can waste less time and have easier access to the projects I love working on. 

[1]:	https://itunes.apple.com/us/app/trello/id461504587?mt=8&uo=4&at=1010laBV
[2]:	http://readdle.com/documents
[3]:	https://itunes.apple.com/us/app/transmit/id917432930?mt=8&uo=4&at=1010laBV
[4]:	https://itunes.apple.com/us/app/drafts-4-quickly-capture-notes/id905337691?mt=8&uo=4&at=1010laBV