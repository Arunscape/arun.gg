---
{"dg-publish":true,"permalink":"/programming/useful-tools/streamlink/"}
---

command to download twitch videos

```bash
streamlink --hls-live-restart --stream-segment-threads 3 --twitch-disable-ads -o "$(date -Iseconds).ts" https://twitch.tv/lostlands best
```