# OCP-Music

The site is published from `index.html`. To add a song, put its MP3 in this
repository and add a `{ title, url }` entry to the matching genre array in
`index.html`. Append entries to preserve existing song share links, which use
playlist positions.

Use file names without commas for songs served from `raw.githubusercontent.com`.
GitHub's raw file response for a name containing a comma can produce a
`Content-Disposition` header that Chrome rejects with
`ERR_RESPONSE_HEADERS_MULTIPLE_CONTENT_DISPOSITION`, even though the file exists
and returns HTTP 200. The playlist uses comma-free copies for affected songs.

If a song cannot start after retries, the player advances to the next track.
