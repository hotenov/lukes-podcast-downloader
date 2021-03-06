# [EN] Readme | Contents

- [DESCRIPTION](#description)
- [INSTALLATION](#installation)
- [OPTIONS](#options)
- [WHAT'S NEW](#whats-new)
- [KNOWN ISSUES](#known-issues)
- [DEMO](#demo)
- [CONTACTS](#contacts)

Useful wiki pages:

- [How to open Terminal (or Command Prompt)](https://github.com/hotenov/LEP-downloader/wiki/How-to-open-Terminal-(or-Command-Prompt))

## DESCRIPTION

**LEP-downloader** is a script for downloading the all FREE episodes of [Luke's ENGLISH Podcast](https://teacherluke.co.uk/archive-of-episodes-1-149/), which have audio, video or text (pdf) files. It requires the Python interpreter, version 3.5+, and it is not platform specific. It should work on your Unix box, on Windows or on macOS. Also you can download the one executable file for your platform. In this case you don't need to install Python (see [Home](https://github.com/hotenov/LEP-downloader/wiki#as-exe) wiki page for details).

It's released under the [MIT License](LICENSE), which means you can modify it, redistribute it or use it however you like as long as you do mention the author of the original script.

You can specify what episode (number) to download or for what period of time, and other options (see [OPTIONS](#options) below)

**Usage** with the Python interpreter:

    python3 LEP-downloader.py [OPTIONS]

**Usage for Windows users (usually with only python 3 installed)** - no need to type `python3`, simply:

    LEP-downloader.py [OPTIONS]

The script doesn't download file if the file already exists in the directory. So you can easily replenish your collection when a new episode is released. **Important:** ALL episodes (audio + pdf) will take up more than 33 GB *(relevant on moment when #621 is the latest episode)* on your drive (HDD, SSD, flash)  and process of downloading will take at least ~2 hours *(depends on the speed of internet connection)*. You must have enough free space for downloading all of them. And of course you will need even more space if you want to download video files. Don't forget about that.  
>The program also looks for files on the disc downloaded by the "first" version. If you want all file names to be in chronological order, I recommend you to delete the old files and download them with the new version.

## INSTALLATION

To copy python script on your computer, the right away for all UNIX users (Linux, macOS, etc.) is using curl. Type command in Terminal:

    curl -L https://raw.githubusercontent.com/hotenov/LEP-downloader/master/LEP-downloader.py -o ~/Downloads/LEP-downloader.py

Where *~/Downloads/* is Downloads folder of active user. You can change it, if you need.

If you do not have curl, you can alternatively use a recent wget:

    wget https://raw.githubusercontent.com/hotenov/LEP-downloader/master/LEP-downloader.py  -O ~/Downloads/LEP-downloader.py

Web browsers users on Windows can click mouse right button and then "Save as..." on [this link](https://raw.githubusercontent.com/hotenov/LEP-downloader/master/LEP-downloader.py)

Also nobody forbids you to clone (download as zip) the entire repository from GitHub.

## OPTIONS

Script execution **without arguments** will try to download all audio files (including audio tracks for video episodes) - no video and pdf files.

To display the list of options, execute script with "-h" or "--help" argument.

## Optional options

    -h, --help            show this help message and exit
    -ep EPISODE, --episode EPISODE
                          Specify episode number (or range of episodes) for
                          downloading
    -pdf, --withpdf       Download PDF files of exported webpage(s)
    -vi, --onlyvideo      Download only video files
    -to PATH, --folder PATH
                          Specify a path to custom download directory (folder)
    -d1 STARTDATE, --startdate STARTDATE
                          Start date for date range filtering. Format "YYYY-MM-
                          DD"
    -d2 ENDDATE, --enddate ENDDATE
                          End date for date range filtering. Format "YYYY-MM-DD"
    --last                Download only the last episode. Options -ep, -d1 and
                          -d2 will be ignored in this case.
    -text, --withoutanymedia
                          Print names list of the posts which have no any media
                          files (only TEXT) for selected episode(s). When used
                          along with --withpdf script downloads pdf files for
                          these posts
    -v, --verbose         Activate verbose mode to display execution steps
                          results
    -q, --quiet           Activate quiet mode. There is no question whether to
                          download files or not. Immediately download them.
    -V, --version         Print script version and exit
    -sj, --savejson       Save database to file "lep-db.json" in the same folder
    --withaddons          Download all additional files (if they added by script
                          author) for selected episode(s)

**Example**:

    python3 LEP-downloader.py -ep 128 -pdf

**For Windows users (usually with only python 3 installed)** - no need to type `python3`, simply:

    LEP-downloader.py -ep 128 -pdf

For more examples and explanation of arguments, see [Home](https://github.com/hotenov/LEP-downloader/wiki#Options) wiki page.

## WHAT'S NEW

The second version was completely rewritten by me. It was divided into two parts for user convenience: **LEP-parser** and **LEP-downloader**. *I'll write about the "LEP-parser" later*.

**LEP-downloader** does not require the installation of additional packages. All works with installed Python 3.5+ or with single [executable file](https://github.com/hotenov/LEP-downloader/wiki#as-exe). It includes several [options](https://github.com/hotenov/LEP-downloader/wiki#Options) to control the process.

It downloads really all available episodes, comparing to the [first version](https://github.com/hotenov/LEP-downloader/wiki/Old-Readme), which skips many episodes.  
Even 'website only' episodes and a couple lost by Luke =).

> I don't want to financially harm Luke in any way, so consider donating to [Luke's English Podcast](https://www.paypal.com/donate/?token=TMJIcfvgEgxmnvr7WNkzDi_cxrZ2_Q_g0SPmsIe6Wc7PETq8T8WHB-Ak_eW03KnD_RBrq0&country.x=GB&locale.x=GB). I just want more people to listen to his podcasts, making them a little easier to download.

## KNOWN ISSUES

> Sometimes several episodes are marked as "NOT FOUND" but if you try to download them separately using `-ep` option they will most likely download successfully.  
If they still "NOT FOUND" after repeating, please [write me](#contacts) a message. I'll try to solve this issue.

[Issue #3](https://github.com/hotenov/LEP-downloader/issues/3)

## DEMO

**Demo screenshots of the script executions**:

![ver-2-screenshot-01](img/ver-2-screenshot-01.png?raw=true "LEP downloader (ver. 2)")

![ver-2-screenshot-02](img/ver-2-screenshot-02.png?raw=true "LEP downloader (ver. 2)")

![ver-2-screenshot-03](img/ver-2-screenshot-03.png?raw=true "LEP downloader (ver. 2)")

## CONTACTS

Any questions, issues and suggestions you can email me: qa@hotenov.com  
Or send me private message: [Facebook](https://www.facebook.com/hotenov), [Twitter](https://twitter.com/_hotenov), [LinkedIn](https://www.linkedin.com/in/hotenov/)
