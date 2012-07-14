## Bashpodder ##
This is my modified version of the bashpodder podcatcher script. The
original is available at <http://lincgeek.org/bashpodder>. I've made
the following modifications:

### Separate folders for each podcast ###

Instead of the default behavior of all podcasts downloaded going into
the same subdirectory, each podcast will use it's own subdirectory. As
such the method of defining podcast feeds in 'bp.conf'. Instead of the
standard:

> http://podcastfeedurl.com/rss

Feeds are defined as:

> http://podcastfeedurl.com/rss feeddir

'feeddir' being the subdirectory for that particular feed. 

### Only filenames placed in log ###

To prevent redownloading files when only the url has changed, only the
filename will be checked instead of the full url.

### Playlist rebuilt after every run ###

Every time the script is run a playlist containing the last files
downloaded will be built and placed in the data directory under the
name 'latest.m3u'.

### Only download the latest file ###

Rather than attempt to download every file in the feed, only the
latest file will be downloaded. 
