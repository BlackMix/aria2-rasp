# aria2-rasp

```php
  aria2:
    container_name: aria2
    image: blackmix/aria2-rasp
    user: "pi"
    ports:
      - "6800:6800/tcp"
      - "6800:6800/udp"
    volumes:
      - "/home/aria2:/home/aria2/downloads" # where downloads dir.
      - "./volumes/aria2/.aria2/:/home/aria2/.aria2/" # dir aria2.session, create that file.
      - "./volumes/_ssl_keys:/home/aria2/keys" # SSL if u need it.
      - "./volumes/aria2/aria2.conf:/home/aria2/aria2.conf" # aria2.conf dir, custom.
    environment:
      TOKEN: <yourTokenHere>
    restart: unless-stopped
```
