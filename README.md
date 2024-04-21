# Isso Demo Instance Config

This is (part of) the "magic" running live at
[isso-comments.de](https://isso-comments.de), enabling anyone to leave a comment
while curtailing vandalism through resetting the comment database every night
and re-populating it with dummy comments.

## Assumptions

- Isso is running via `gunicorn` via a systemd service called
  `gunicorn-isso.service`
- Isso is running under user `isso` and `/home/isso` is accessible
- Config points to `/home/isso/dbs/isso-comments.db` as database

## Install

1. `cp comments-demo.db /home/isso/`
2. `cp isso-restarter.{timer,service} /etc/systemd/system/`
3. `sudo systemd enable --now isso-restarter.service`

## License

MIT, see [LICENSE](LICENSE).
