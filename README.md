# Windows-setup
## The shortest path to computing happiness after a ground zero event
This assumes a Windows 10 setup.  First start Windows and delete any obviously nasty things.  Connect to the internet with the provided cruft and login with the Microsoft user ID.  Check Windows Defender is scanning and updating.  Check Onedrive.  Access the Windows Insider Programme Slow track, OS builds only.

Transfer the Documents folder to C:\Users\lewis\ (probably).

Setup linux subsystem Ubuntu.  Except maybe go easy on this step which possibly destroyed the last one.

Install [Zotero](https://www.zotero.org/), make sure to set the linked attachment base directory (Edit - Preferences - Advanced - Files and Folders to allow documents to open from the citation library.

Install [Microsoft R Open](https://mran.microsoft.com/download/).

Install [Rstudio](https://www.rstudio.com/products/rstudio/download/).

[Install](https://git-for-windows.github.io/) and [configure](happygitwithr) git.  Test and confirm.

Install [miktex](https://miktex.org/download) and verify rstudio is knitting correctly.

Install and check a git client, [GitKraken](https://www.gitkraken.com/) or [Sourcetree](https://www.sourcetreeapp.com/).  Not sure which is better yet.

Get the VPNs set up.  For example, the [UoE help pages](https://www.ed.ac.uk/information-services/computing/desktop-personal/vpn) or for the [Cisco AnyConnect VPN client](https://www.ed.ac.uk/information-services/computing/desktop-personal/vpn/vpn-cisco-client/cisco-anyconnect-ssl-client-windows).

I'm not sure how necessary this step is but it works: [MobaXterm download](https://mobaxterm.mobatek.net/download.html) then [WinSCP](https://winscp.net/eng/download.php) to allow the VPN bash access and file system GUI explorer that mostly works so far.  Log into the VPN then form a tunnel but be careful with the relative pathways after that, for the WinSCP access.  Should work with any VPN at all.  On the other hand built-ins should work, particularly Git bash and maybe the git clients.  Must try that some time for leanness.

Install [firefox 64bit]() and login.
Install keepass

Install libreoffice and check zotero and latex integration

Install [foxit](https://www.foxitsoftware.com/pdf-reader/), just the reader, not Phantom.

Install [vlc](https://get.videolan.org/vlc/2.2.6/win64/vlc-2.2.6-win64.exe) and [Audacity](https://www.fosshub.com/Audacity.html/audacity-win-2.1.3.exe)

Install gimp from Partha and check latest RAW import shenanigans

Install notepad++

Install teamviewer

Install the very annoying Anaconda for python 3 and verify notebooks.
