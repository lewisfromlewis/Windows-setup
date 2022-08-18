# Windows-setup
## The shortest path to computing happiness after a ground zero event
This assumes a Windows 10 setup.  First start Windows and delete any obviously nasty things.  Connect to the internet with the provided cruft and login with the Microsoft user ID.  Check Windows Defender is scanning and updating.  Check Onedrive is not doing anything too stupid.  Access the Windows Insider Programme Slow track, OS builds only.

Switch on system restore!
Make sure the user is not set with a space, like "Lewis Campbell", because that's stupid.

Transfer the Documents folder to C:\Users\lewis\ (probably).

Setup linux subsystem using Powershell `wsl --install` as [described](https://docs.microsoft.com/en-us/windows/wsl/install). Install the aws cli, and then the aws sam cli including Docker, for [linux](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install-linux.html), for compatibility with the development environment.

`pandoc`, `pdfmerge`, `ffmpeg` unless they're installed with other things. Check back at the end.

Easy ones: Takoboto, Pleco, Chinese, Gàidhlig, Japanese inputs, kindle, dropbox, garmin express, metacreator, signal, slack, steam, whatsapp, zoom.

Install the java jdk.  Probably stick to 8 for now to avoid LibreOffice conflicts. More to follow here with the json approach.

Install [Zotero](https://www.zotero.org/), make sure to set the linked attachment base directory (Edit - Preferences - Advanced - Files and Folders to allow documents to open from the citation library.

Install [Microsoft R Open](https://mran.microsoft.com/download/). Check that the `.libPaths()` refers to the location with all the goodies and if not, trawl through help(.libPaths) until about 1am until you find the bit saying "add or edit the R_LIBS_USER environment variable with the value of the desired library location". Install [RTools](https://cran.r-project.org/bin/windows/Rtools/) correct version to allow source builds. Update packages.  Yes all.

Install [Rstudio](https://www.rstudio.com/products/rstudio/download/).  The dependencies get annoying very quickly especially as I'm not working across a whole organisation. Try updating RProfile.site in the R distribution with `options(repos = c(CRAN = "https://cran.revolutionanalytics.com"))` just below the section on checking for a timepoint repo. Check at the end of the page for the list of packages you need if you're offline, and which you would forget otherwise.

[Install](https://git-for-windows.github.io/) and [configure](happygitwithr) git.  Test and confirm.

Install tinytex from rstudio and verify it's knitting correctly.

Install and check a git client, [GitKraken](https://www.gitkraken.com/) or [Sourcetree](https://www.sourcetreeapp.com/).  Not sure which is better yet.

Get the VPNs set up.  For example, the [UoE help pages](https://www.ed.ac.uk/information-services/computing/desktop-personal/vpn) or for the [Cisco AnyConnect VPN client](https://www.ed.ac.uk/information-services/computing/desktop-personal/vpn/vpn-cisco-client/cisco-anyconnect-ssl-client-windows).

I'm not sure how necessary this step is but it works: [MobaXterm download](https://mobaxterm.mobatek.net/download.html) then [WinSCP](https://winscp.net/eng/download.php) to allow the VPN bash access and file system GUI explorer that mostly works so far.  Log into the VPN then form a tunnel but be careful with the relative pathways after that, for the WinSCP access.  Should work with any VPN at all.  

Install [firefox 64bit](https://www.mozilla.org/en-US/firefox/) and login, add the [Zotero connector](https://www.zotero.org/download/connectors).

Install [keepass](https://keepass.info/).

Install [libreoffice](https://www.libreoffice.org/download/download/), 6.0.2.1 works with TeXmaths which is everything to me. Check zotero and [latex](https://extensions.libreoffice.org/extensions/texmaths-1) integration.

Install [foxit](https://www.foxitsoftware.com/pdf-reader/), just the reader, not Phantom.

Install [vlc](https://get.videolan.org/vlc/2.2.6/win64/vlc-2.2.6-win64.exe) and maybe [Audacity](https://www.fosshub.com/Audacity.html/audacity-win-2.1.3.exe) and definitely [Waveform](https://www.tracktion.com/products/waveform-free), then think about Equator for the sounds. That still means an ASIO is needed, so [ASIO4ALL](https://www.asio4all.org/). Consider [OpenShot](https://www.openshot.org/).

Install gimp from [Partha](https://www.partha.com/) and check latest RAW import shenanigans

Install notepad++ because it's tiny. Also install Atom for now until it's obvious which is nicer.

Consider [teamviewer](https://www.teamviewer.com/en/download/windows/), it's surprisingly small, best for meetings5 and I don't have any proof it's watching me at my ablutions.

Have a think about the very annoying Anaconda for python 3 and verify notebooks, or whether Reticulate is sufficient.

Put [calibre](https://calibre-ebook.com/download_windows64) on it, it's been useful for notes and otherwise unreadable stuff.  On the same track, use [Denemo](http://www.denemo.org/downloads-page/) for the music.  And try, for any favour, to write something,  it's been too long.

To do: figure out how to setup a VPN to your shambolic backups and how to run R in an RStudio server instance so you can scale it all the way up when you need to.  And how to get a SQL server running.

## SQL server 
I'm still not totally sure whether I needed to install postgre at all because it's included with Ubuntu... but is it included with wsl Ubuntu? This might work if so:
`apt-get install postgresql-12`

Anyway, to install a specific new version the script is needed:

`sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
sudo apt-get update
sudo apt-get -y install postgresql`

Then once something is installed, 
`service postgresql status`
and maybe need
`service postgresql restart`
then
`sudo -u postgres psql`

## Those packages
`tidyverse`
`devtools`
NMM loadorder.txt:
GameMode=Fallout4
Fallout4.esm=1
DLCRobot.esm=1
DLCworkshop01.esm=1
DLCCoast.esm=1
DLCworkshop02.esm=1
DLCworkshop03.esm=1
DLCNukaWorld.esm=1
ccbgsfo4005-bluecamo.esl=1
ccbgsfo4024-pacamo03.esl=1
ccgcafo4005-factionws05hrpink.esl=1
ccgcafo4011-factionws11vt.esl=1
ccgcafo4022-factionas11vt.esl=1
simsettlements.esm=1
ArmorKeywords.esm=1
Unofficial Fallout 4 Patch.esp=1
everyonesbestfriend.esp=1
conquest.esp=1
crimetown.esp=1
trainbar.esp=1
NoSpinUpPlusCoreFix.esp=1
3dscopes-framework.esp=1
3dscopes.esp=1
3dscopes-AddToSpawnList.esp=1
Marmo1233 - PowerArmorAirdrop.esp=1
StartMeUp.esp=1
Crafting Mastery - Patch Sim Settlements.esp=1
Armorsmith Extended.esp=1
Crafting Mastery.esp=1
EnclaveX02.esp=1
NanoSuit.esp=1
NanoSuit_AWKCR_AE.esp=1
