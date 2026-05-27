Issue 6:​

1. vi /etc/dnsmasq.conf​

port=5353​

listen-address=192.168.168.1​

bind-interfaces​

no-resolv​

no-hosts​

no-poll​

cache-size=1000​

log-queries​

log-facility=-​

server=127.0.0.1#5354​

(and restart dnsmasq daemon)​

​

2. python3 i6_server.py --host 127.0.0.1 --port 5354 --rdlen 6 –debug &​

3. python3 i6_client.py --dnsmasq-host 192.168.168.1 --dnsmasq-port 5353 --timeout 5.0 --count 3​