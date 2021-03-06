# Wireguard + SOCKS proxy all in one

This container image runs Wireguard + SOCKS proxy.

```bash
docker run 
    --name wireguardproxy
    --privileged
    -v /path/to/conf/wgcf.conf:/etc/wireguard/wgcf.conf
    -p 1080:1080
    diwu1989/wireguardproxy
```

Default SOCKS5 proxy auth is `proxy:wireguard`
```
curl --socks5 proxy:wireguard@127.0.0.1:1080 https://api.ipify.org
```

Built images published @ https://hub.docker.com/r/diwu1989/wireguardproxy
