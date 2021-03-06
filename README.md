# Windows-setup
## The shortest path to computing happiness after a ground zero event
This assumes a Windows 10 setup.  First start Windows and delete any obviously nasty things.  Connect to the internet with the provided cruft and login with the Microsoft user ID.  Check Windows Defender is scanning and updating.  Check Onedrive.  Access the Windows Insider Programme Slow track, OS builds only.

Transfer the Documents folder to C:\Users\lewis\ (probably).

Setup linux subsystem Ubuntu.  Except maybe go easy on this step which possibly destroyed the last one.

Install the java jdk.  Stick to 8 for now to avoid LibreOffice conflicts.

Install [Zotero](https://www.zotero.org/), make sure to set the linked attachment base directory (Edit - Preferences - Advanced - Files and Folders to allow documents to open from the citation library.

Install [Microsoft R Open](https://mran.microsoft.com/download/). Check that the `.libPaths()` refers to the location with all the goodies and if not, trawl through help(.libPaths) until about 1am until you find the bit saying "add or edit the R_LIBS_USER environment variable with the value of the desired library location". Update packages.  Yes all.

Install [Rstudio](https://www.rstudio.com/products/rstudio/download/).  Check at the end of the page for the list of packages you need if you're offline, and which you would forget otherwise.

[Install](https://git-for-windows.github.io/) and [configure](happygitwithr) git.  Test and confirm.

Install [miktex](https://miktex.org/download) and verify rstudio is knitting correctly.

Install and check a git client, [GitKraken](https://www.gitkraken.com/) or [Sourcetree](https://www.sourcetreeapp.com/).  Not sure which is better yet.

Get the VPNs set up.  For example, the [UoE help pages](https://www.ed.ac.uk/information-services/computing/desktop-personal/vpn) or for the [Cisco AnyConnect VPN client](https://www.ed.ac.uk/information-services/computing/desktop-personal/vpn/vpn-cisco-client/cisco-anyconnect-ssl-client-windows).

I'm not sure how necessary this step is but it works: [MobaXterm download](https://mobaxterm.mobatek.net/download.html) then [WinSCP](https://winscp.net/eng/download.php) to allow the VPN bash access and file system GUI explorer that mostly works so far.  Log into the VPN then form a tunnel but be careful with the relative pathways after that, for the WinSCP access.  Should work with any VPN at all.  On the other hand built-ins should work, particularly Git bash and maybe the git clients.  Must try that some time for leanness.

Install [firefox 64bit](https://www.mozilla.org/en-US/firefox/) and login, add the [Zotero connector](https://www.zotero.org/download/connectors).

Install [keepass 2.37](https://keepass.info/).

Install [libreoffice 6](https://www.libreoffice.org/download/download/), 6.0.2.1 works with TeXmaths which is everything to me. Check zotero and [latex](https://extensions.libreoffice.org/extensions/texmaths-1) integration.

Install [foxit](https://www.foxitsoftware.com/pdf-reader/), just the reader, not Phantom.

Install [vlc](https://get.videolan.org/vlc/2.2.6/win64/vlc-2.2.6-win64.exe) and [Audacity](https://www.fosshub.com/Audacity.html/audacity-win-2.1.3.exe)

Install gimp from Partha and check latest RAW import shenanigans

Install notepad++

Install [teamviewer](https://www.teamviewer.com/en/download/windows/), it's surprisingly small, best for meetings5 and I don't have any proof it's watching me at my ablutions.

Install the very annoying Anaconda for python 3 and verify notebooks.

Put [calibre](https://calibre-ebook.com/download_windows64) on it, it's been useful for notes and otherwise unreadable stuff.  On the same track, use [Denemo](http://www.denemo.org/downloads-page/) for the music.  And try, for any favour, to write something,  it's been too long.

To do: figure out how to setup a VPN to your shambolic backups and how to run R in an RStudio server instance so you can scale it all the way up when you need to.  And how to get a SQL server running.

## Those packages
`tidyverse`
`devtools`
use [MRAN](https://mran.microsoft.com/) for the R source because the it can take full advantage of the computer and RStudio can take full advantage of R.
