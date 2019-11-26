# nmap

Another docker based nmap.

[Docker hub official image](https://hub.docker.com/r/ociotec/nmap).

## How to run it

For instance, to get all open ports in all your local network (change net at the end of command to yours):

```
docker run --rm ociotec/nmap nmap -p- 192.168.1.0/24
```

Same command but with XML output (readable by browser due to webxml extension):

```
docker run --rm --volume $(pwd):/tmp/report ociotec/nmap nmap -p- -oX /tmp/report/report.xml --webxml 192.168.1.0/24
```

## More info about nmap

* [nmap reference guide](https://nmap.org/book/man.html)
* [Nmap cheat sheet](https://hackertarget.com/nmap-cheatsheet-a-quick-reference-guide/)
