# rarbg → rss

Adapter for [Torrent API](https://torrentapi.org/apidocs_v2.txt) that serves search results as broadcatching-ready RSS feed.

## Usage

`/` main endpoint, pass parameters as you would pass them to API. 

Note that API has rate limit of one request per two seconds.

### Convenience methods

`/imdb/<imdb_id>` search by imdb (equals to `/?mode=search&search_imdb=<imdb_id>`)

`/tvdb/<tvdb_id>` search by tvdb (equals to `/?mode=search&search_tvdb=<tvdb_id>`)

`/search/<search_term>` search by string (equals to `/?mode=search&search_string=<search_term>`)

### Additional filters

`category` filter by category, specify multiple categories like this:  `44;45`

`limit` number of results: `25`, `50` or `100` (default: `25`)

`sort` order by `seeders`, `leechers` (default: `last`)

`min_seeders` and `min_leechers`

`ranked=0` get non-scene releases

All parameters can be mixed together and work with convenience methods.

### Categories

```
 4 XXX (18+)
14 Movies/XVID
48 Movies/XVID/720
17 Movies/x264
44 Movies/x264/1080
45 Movies/x264/720
47 Movies/x264/3D
42 Movies/Full BD
46 Movies/BD Remux
18 TV Episodes
41 TV HD Episodes
23 Music/MP3
25 Music/FLAC
27 Games/PC ISO
28 Games/PC RIP
40 Games/PS3
32 Games/XBOX-360
33 Software/PC ISO
35 e-Books
```