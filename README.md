# Ping.cr

The minimum ICMP echo handling shard.

This shard is only an experiment to use the raw socket in the Crystal language.

## Installation

1. Add the dependency to your `shard.yml`:
```yaml
dependencies:
  ping:
    github: arcage/ping.cr
```
2. Run `shards install`

## Usage

```crystal
# src/ping_command.cr
require "ping"

Ping.command(ARGV.shift)
```

```shell
$ sudo crystal src/ping_command.cr 192.0.2.1
PING 192.0.2.1: 56 data bytes
64 bytes from 192.0.2.1: icmp_seq=0 ttl=253 time=1.903 ms
64 bytes from 192.0.2.1: icmp_seq=1 ttl=253 time=1.466 ms
64 bytes from 192.0.2.1: icmp_seq=2 ttl=253 time=1.355 ms
64 bytes from 192.0.2.1: icmp_seq=3 ttl=253 time=2.115 ms
64 bytes from 192.0.2.1: icmp_seq=4 ttl=253 time=2.074 ms

--- 192.0.2.1 ping statistics ---
5 packets transmitted, 5 packets received, 0% packet loss
round-trip min/avg/max/stddev = 1.355/1.783/2.115/0.346 ms
```

_NOTE: Because this shard use RAW SOCKET, you need `sudo` when execute the program with this shard._

## Contributors

- [ʕ·ᴥ·ʔAKJ](https://github.com/arcage) - creator and maintainer
