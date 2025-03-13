usage: qbtools.py [-h] {prune,limiter,tagging,reannounce,orphaned} ...

qBittorrent API Client

positional arguments:
  {prune,limiter,tagging,reannounce,orphaned}

options:
  -h, --help            show this help message and exit
usage: qbtools.py prune [-h] --include-tag [mytag ...]
                        [--exclude-tag [mytag ...]]
                        [--include-category [mycategory ...]]
                        [--exclude-category [mycategory ...]] [--dry-run]
                        [--with-data] [-c CONFIG] -s SERVER -p PORT
                        [-U USERNAME] [-P PASSWORD]

options:
  -h, --help            show this help message and exit
  --include-tag [mytag ...]
                        Include torrents containing all of these tags, can be
                        repeated multiple times
  --exclude-tag [mytag ...]
                        Exclude torrents containing any of these tags, can be
                        repeated multiple times
  --include-category [mycategory ...]
                        Include torrents only from category that matches this
                        pattern, can be repeated multiple times. If not
                        specified, all categories are included
  --exclude-category [mycategory ...]
                        Exclude torrents from category that matches this
                        pattern, can be repeated multiple times
  --dry-run             Do not delete torrents
  --with-data           Delete torrents with data
  -c, --config CONFIG   Path to configuration file
  -s, --server SERVER   qBittorrent server address
  -p, --port PORT       qBittorrent server port
  -U, --username USERNAME
                        Username for qBittorrent
  -P, --password PASSWORD
                        Password for qBittorrent
usage: qbtools.py limiter [-h] --sabnzbd-host SABNZBD_HOST
                          [--sabnzbd-port SABNZBD_PORT]
                          --sabnzbd-apikey SABNZBD_APIKEY
                          [--max-line-speed-mbps MAX_LINE_SPEED_MBPS]
                          [--limit-percent LIMIT_PERCENT]
                          [--max-percent MAX_PERCENT] [--interval INTERVAL]
                          [-c CONFIG] -s SERVER -p PORT [-U USERNAME]
                          [-P PASSWORD]

options:
  -h, --help            show this help message and exit
  --sabnzbd-host SABNZBD_HOST
                        The host of the SabNZBD server
  --sabnzbd-port SABNZBD_PORT
                        The port of the SabNZBD server
  --sabnzbd-apikey SABNZBD_APIKEY
                        The API key for the SabNZBD server
  --max-line-speed-mbps MAX_LINE_SPEED_MBPS
                        The maximum line speed in Mbps
  --limit-percent LIMIT_PERCENT
                        The percentage of the line speed to limit to when both
                        are downloading
  --max-percent MAX_PERCENT
                        The maximum percentage of the line speed to limit to
                        when both are not downloading
  --interval INTERVAL   The interval to check the speeds in seconds
  -c, --config CONFIG   Path to configuration file
  -s, --server SERVER   qBittorrent server address
  -p, --port PORT       qBittorrent server port
  -U, --username USERNAME
                        Username for qBittorrent
  -P, --password PASSWORD
                        Password for qBittorrent
usage: qbtools.py tagging [-h] [--exclude-category [mycategory ...]]
                          [--exclude-tag [mytag ...]] [--added-on]
                          [--duplicates] [--expired] [--last-activity]
                          [--not-linked] [--not-working] [--sites]
                          [--tracker-down] [--unregistered] [-c CONFIG]
                          -s SERVER -p PORT [-U USERNAME] [-P PASSWORD]

options:
  -h, --help            show this help message and exit
  --exclude-category [mycategory ...]
                        Exclude all torrent with this category, can be
                        repeated multiple times
  --exclude-tag [mytag ...]
                        Exclude all torrents with this tag, can be repeated
                        multiple times
  --added-on            Tag torrents with added date (last 24h, 7 days, 30
                        days, etc)
  --duplicates          Tag torrents with the same content path
  --expired             Tag torrents that have an expired ratio or seeding
                        time (defined in config.yaml)
  --last-activity       Tag torrents with last activity date (last 1d, 7 days,
                        30 days, etc)
  --not-linked          Tag torrents with files without hardlinks or symlinks,
                        use with filtering by category/tag
  --not-working         Tag torrents with not working tracker status
  --sites               Tag torrents with site names (defined in config.yaml)
  --tracker-down        Tag torrents with temporarily down trackers
  --unregistered        Tag torrents with unregistered tracker status message
  -c, --config CONFIG   Path to configuration file
  -s, --server SERVER   qBittorrent server address
  -p, --port PORT       qBittorrent server port
  -U, --username USERNAME
                        Username for qBittorrent
  -P, --password PASSWORD
                        Password for qBittorrent
usage: qbtools.py reannounce [-h] [--max-age MAX_AGE]
                             [--max-retries MAX_RETRIES] [--interval INTERVAL]
                             [--process-seeding] [-c CONFIG] -s SERVER -p PORT
                             [-U USERNAME] [-P PASSWORD]

options:
  -h, --help            show this help message and exit
  --max-age MAX_AGE     The maximum age of a torrent in seconds to reannounce.
  --max-retries MAX_RETRIES
                        The maximum number of reannounce retries for a
                        torrent.
  --interval INTERVAL   The interval to process reannouncements in seconds.
  --process-seeding     Process seeding torrents as well.
  -c, --config CONFIG   Path to configuration file
  -s, --server SERVER   qBittorrent server address
  -p, --port PORT       qBittorrent server port
  -U, --username USERNAME
                        Username for qBittorrent
  -P, --password PASSWORD
                        Password for qBittorrent
usage: qbtools.py orphaned [-h] [--exclude-pattern [mypattern ...]]
                           [--dry-run] [-c CONFIG] -s SERVER -p PORT
                           [-U USERNAME] [-P PASSWORD]

options:
  -h, --help            show this help message and exit
  --exclude-pattern [mypattern ...]
                        Exclude pattern, can be repeated multiple times
  --dry-run             Do not delete any data on disk
  -c, --config CONFIG   Path to configuration file
  -s, --server SERVER   qBittorrent server address
  -p, --port PORT       qBittorrent server port
  -U, --username USERNAME
                        Username for qBittorrent
  -P, --password PASSWORD
                        Password for qBittorrent
