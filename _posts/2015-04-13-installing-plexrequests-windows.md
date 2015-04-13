---
title: Installing Plex Requests on Windows
layout: post
date: 2015-04-13
---

<p class="intro"><span class="dropcap">F</span>or those currently using Windows for running <a href="http://plexrequests.8bits.ca">Plex Requests</a> it can seem a bit intimidating to get things up and running, not to mention updating to new versions! I hope to give a quick rundown on how to do things using <a href="http://git-scm.com/">Git</a>which allows you the update and switch branches the easiest.</p>

###Installation
The only requirement is Git which you can download and install from [here](http://git-scm.com/downloads). The standard installation options should suffice as we're going to be using the GUI component that is installed. I was going to use the `bash` script but it seems you can't copy or paste into it which seems silly.

Once the installation is complete, open up `Git GUI` from your start menu. From the options listed, select `Clone Existing Repository`. For the source enter the clone URL for the project, `https://github.com/lokenx/plexrequests-meteor.git`. For the target location, choose the folder you would like to install Plex Requests into, from here on out we'll be using `C:\plexrequests`. Then press Clone to start the download process.

You should now have the folder you specified with the projects file downloaded into. You can open up your command prompt, navigate to the folder, and run `meteor` to get Plex Requests running locally at `http://locahost:3000/`. Your database is saved in `C:\plexrequests\.meteor\local` if you want to make backup copies of it. You can also safely close the `Git GUI` application as it's not needed to be open all the time.

###Updating
When a new version comes out, a bug release is pushed, or you just want to update to the latest copy it's super simple. Stop the `meteor` process from the command line with `ctrl + c`. Open up `Git GUI` and from the main screen you should see the repository we made earlier. If not, select `Open Existing Repository` and point it towards the folder where Plex Requests is installed. In the new window select the `Remote` menu, highlight the `Fetch` option and select `origin`. A new window should open that shows you the progress and status of any updates that have been applied, and once complete show `Success`. If that's the case you're all done, Plex Requests is now updated to the latest version!

###Switching to dev
If you feel adventurous, or want to try out some new feature that's currently under development you can easily switch to the dev branch. Using `Git GUI` open up your current repository. Select the `Branch` menu and then select `Create`. In the new window choose `Match Tracking Branch Name` at the top. In the next section select the branch you want to switch to, be it `dev` or `master` (if you want to switch back to the main releases). After a few moments the window should close and the main Git screen should say `Checked out` whichever repository you selected in the lower left. You're now running on the latest release of whichever branch you selected.

Hopefully you now have Plex Requests up and running on your machine locally, as well as have the ability to easily update it as new versions get released. If if you're still having issues please visit the [Plex Requests site](http://plexrequests.8bits.ca/), post a [GitHub issue](https://github.com/), or post on the [Plex Forums](https://forums.plex.tv/index.php/topic/151899-plex-movie-requests/)
