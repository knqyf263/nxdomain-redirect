# nxdomain-redirect

## Build

```
$ git clone https://github.com/knqyf263/nxdomain-redirect.git
$ cd nxdomain-redirecct
$ docker built -t nxdomain-redirect .
$ docker run --rm -it -p 53:53/udp nxdomain-redirect
```

## Query

```
$ dig @127.0.0.1 nxdomain.example.com

; <<>> DiG 9.10.6 <<>> @127.0.0.1 nxdomain.example.com
; (1 server found)
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 40079
;; flags: qr aa rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 4096
;; QUESTION SECTION:
;nxdomain.example.com.          IN      A

;; ANSWER SECTION:
example.com.            3600    IN      A       192.168.1.4

;; Query time: 1 msec
;; SERVER: 127.0.0.1#53(127.0.0.1)
;; WHEN: Thu Apr 25 15:15:55 JST 2019
;; MSG SIZE  rcvd: 65
```

