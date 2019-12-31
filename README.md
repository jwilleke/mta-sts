# mta-sts

## MTA-STS Willeke.com

Data taken from: <https://admin.google.com/ac/apps/cs/diagnostic>

### DNS Records

```bash
_mta-sts v=STSv1;id=1577377920599;
_smtp._tls v=TLSRPTv1;rua=mailto:reports@willeke.com;
```

## Policy file

Content should be as in file [docs/.well-known/mta-sts.txt](docs/.well-known/mta-sts.txt)

### URLs

Github URL:
<https://jwilleke.github.io/mta-sts/.well-known/mta-sts.txt>

Custom Domain URL:
<https://mta-sts.willeke.com/.well-known/mta-sts.txt>

## Testing

Testing GitHub DNS

```bash
dig jwilleke.github.io +nostats +nocomments +nocmd

; <<>> DiG 9.10.6 <<>> jwilleke.github.io +nostats +nocomments +nocmd
;; global options: +cmd
;jwilleke.github.io.		IN	A
jwilleke.github.io.	3599	IN	A	185.199.111.153
jwilleke.github.io.	3599	IN	A	185.199.109.153
jwilleke.github.io.	3599	IN	A	185.199.110.153
jwilleke.github.io.	3599	IN	A	185.199.108.153
```
Command appearsa to be working.

Testing willeke DNS

```bash
dig mta-sts.willeke.com +nostats +nocomments +nocmd

; <<>> DiG 9.10.6 <<>> jwilleke.github.ioo +nostats +nocomments +nocmd
;; global options: +cmd
;jwilleke.github.ioo.		IN	A
.			86391	IN	SOA	a.root-servers.net. nstld.verisign-grs.com. 2019122901 1800 900 604800 86400
```

Command is FAILING bnut gets to github.

### Testing Domain Forwarding

<https://jwilleke.github.io/mta-sts/index.html>

Github URL Seems to work:

<https://jwilleke.github.io/mta-sts/.well-known/mta-sts.txt>

These work but not with TLS:
<http://mta-sts.willeke.com/mta-sts/.well-known/mta-sts.txt>
<https://mta-sts.willeke.com/mta-sts/.well-known/mta-sts.txt>

<https://mta-sts.willeke.com/index.html>
