# youtube-dl-script

#!/bin/sh

cd /var/services/homes/admin/Media/YouTube
/volume1/@appstore/python3/bin/youtube-dl --playlist-reverse \
		   --dateafter now-2weeks \
		   --download-archive /var/services/homes/admin/Media/YouTube/downloaded.txt \
		   -i \
		   -o "%(uploader)s/%(playlist)s/%(playlist)s - S01E%(playlist_index)s - %(title)s [%(id)s].%(ext)s" \
		   --add-metadata \
		   --write-thumbnail \
		   --batch-file=/var/services/homes/admin/Media/YouTube/channel_list.txt
