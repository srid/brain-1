# iOS experiment 1: changing and tinkering with a Wordpress site theme
As I [mentioned last week][1], I'm trying to make my iPad Air 2 actually useful in my life. Currently, it's a rarely used content portal despite being almost as powerful as my MacBook Pro and having a fantastic app ecosystem. 

Plenty of folks have talked about the beauty of being able to code on an iPad - there's apps like [Coda][2] and [Textastic][3] that have been germinating for years in the App Store - but there's so much more to web & software development than just writing code. You need a local development environment. You need to be able to manage changes to your code via Git or Subversion. You need to be able to show people real changes before pushing those changes to your live site or app. You need to be able to read and manipulate data. There's plenty more I can't even think of, since - hey now - I'm not actually a full-time developer.

That said, I manage a few sites built in self-hosted [Wordpress][4], one of which is this site. I got tired of having to find and fix bugs with the old theme, so I wanted to see if I could simply change a theme and hack it to my liking, all via my iPad.

### Why is this not so intuitive to the untrained eye?
Wordpress has an amazing theme directory of its own, which allows for direct installs to your website; plus there are thousands of premium theme repositories across the Internet which package beautiful themes in nice .zip packages, which can be extracted easily within your hosting environment for use. I've been doing this for years and it's second nature at this point to launch a Wordpress site and tinker with countless themes. However, this is a bit harder to do on iOS:

- [Wordpress' iOS app][5] has no awareness of its own theme directory;
- There's no true in-house file management solution in iOS;
- iOS' handling of .zip files in itself is murky at best;
- There's no obvious way to set up a local environment of your Wordpress site on iOS to tinker with the theme before pushing it live 

So, how should we deal with this?

### Finding and getting a new theme
As I mentioned before, it's really easy to find Wordpress themes on the Internet - just Google it. When I find a theme I like, I need to download the .zip file containing its assets and somehow get it onto my hosting platform.

I've come to really appreciate [Readdle's Documents app][6] for all my file downloads and management. It has its own built-in browser, which handles file downloads much more seamlessly than Safari's stock file handling. I've found that some Wordpress theme providers require a login to access a theme's files (ThemeForest, for example), so having Documents for both the logged-in experience on one of these sites and the downloads I need to perform is really helpful. I can then open up and look at the files within Documents, and upload them straight to my FTP server provided by my hosting provider - all within Documents.

### Testing the theme out
Web & software developers commonly refer to a 'local' environment for making changes to their code & testing those changes. I haven't yet found a good way to do this all directly on my iOS device; however, with websites, it's pretty easy to set up a private sandbox to test out new themes before pushing them to my live site.

I use [Namecheap][7] for both my domains and shared hosting; they give me a pretty robust SFTP server to host all my files for my websites. I've set up my 3 main websites to point to this server, as well as 3 "sandboxed" versions of those websites in a subdirectory - /sandbox/brandonlucasgreen/, for example. In that folder is another Wordpress install which is private to the world and only accessible to me, which I set up simply through the cPanel interface. Setting up a new Wordpress install in iOS Safari isn't quite as speedy as it is on my MacBook Pro, but it's not terribly hard to get done.

What **doesn't** work well on a 9.7" screen is Wordpress.com's stock post editor. 
![][image-1]

Thank goodness for [Ulysses][8], which is so much more pleasant to look at, extremely good at organizing my writing (both long- and extremely short-form), and can get my posts to Wordpress via a simple [Workflow][9].[^1]
![][image-2]

Having a sandbox to break things within is great, but I also wanted to try some sort of revision management on the iPad. Turns out there's a great app for that in [Working Copy][10]. I love this thing - I can make simple code changes right inside the app, push them to the sandbox git repo I created, see the changes instantly, and then push them to Github and production once I'm satisfied.
![][image-3]
![][image-4]

### Messing with data
Occasionally I need to hack together posts and other Wordpress settings in various states, and sometimes it's easier to do that directly in the database Wordpress uses, rather than in Wordpress' (admittedly slow) admin interface. Wordpress operates on MySQL, and I've found that [Navicat's MySQL client][11] for iOS is a solid app for dealing with this.
---- 
This is just a start, but after messing around with a few apps and getting comfortable with a smaller screen, I'm reasonably confident that I can manage my website entirely from an iPad. Next up: working with audio on an ipad.

[^1]:	They're even adding native Wordpress support in Ulysses 2.6 coming soon!

[1]:	http://brandonlucasgreen.com/moving-to-ios-an-experiment-in-creative-restraint/
[2]:	https://itunes.apple.com/us/app/coda/id500906297?mt=8&uo=4&at=1010laBV
[3]:	https://itunes.apple.com/us/app/textastic-code-editor-6/id1049254261?mt=8&uo=4&at=1010laBV
[4]:	http://wordpress.org
[5]:	https://itunes.apple.com/us/app/wordpress/id335703880?mt=8&uo=4&at=1010laBV
[6]:	https://itunes.apple.com/us/app/documents-5-fast-pdf-reader/id364901807?mt=8&uo=4&at=1010laBV
[7]:	http://namecheap.com
[8]:	https://itunes.apple.com/us/app/ulysses-mobile/id950335311?mt=8&uo=4&at=1010laBV
[9]:	https://itunes.apple.com/us/app/workflow-powerful-automation/id915249334?mt=8&uo=4&at=1010laBV
[10]:	https://itunes.apple.com/us/app/working-copy-powerful-git/id896694807?mt=8&uo=4&at=1010laBV
[11]:	https://itunes.apple.com/us/app/navicat-for-mysql-your-mobile/id688128940?mt=8&uo=4&at=1010laBV

[image-1]:	http://i2.wp.com/brandonlucasgreen.com/wp-content/uploads/2016/04/ipad-wordpress-admin.jpeg?fit=640,480
[image-2]:	http://i1.wp.com/brandonlucasgreen.com/wp-content/uploads/2016/04/ulysses-on-ipad.jpeg?fit=640,480
[image-3]:	http://i1.wp.com/brandonlucasgreen.com/wp-content/uploads/2016/04/working-copy-code-editor.jpeg?fit=640,480
[image-4]:	http://i1.wp.com/brandonlucasgreen.com/wp-content/uploads/2016/04/working-copy-and-safari-side-by-side.jpeg?fit=640,480