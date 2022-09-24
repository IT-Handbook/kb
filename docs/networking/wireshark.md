---
title: WIRESHARK
sidebar_position: 10
---

## Filter Traffic by Source or Destrination IP
```
ip.dst==8.8.8.8
ip.src==8.8.8.8
```

## Filter traffic by specific address
```
ip.addr==8.8.8.8
```

## Filter traffic using protocol
```
dns
dns and http
dns or http
```

## Filter traffic using the Port number
```
tcp.port == 443
```

## Filter TCP traffic using Flags
```
tcp.analysis.flags
```

## Filter traffic using Knot (Exclude)
```
!(arp or dns or icmp)
```

## Filtering a conversation
```
tcp.stream
```

## Filtering using particular text in a packet
```
tcp contains facebook
udp contains facebook
```

## Filter using the HTTP Response code
```
http.response.code == 200
```

## Name Resolution in Wireshark (Enable in Preferences | Not Enabled by default)


## Filtering traffic with geoip (Example showing excluding U.S. based traffic)
```
ip and not ip.geoip.country == "United States"
```