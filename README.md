# mta-sts

## MTA-STS Willeke.com

Data taken from: <https://admin.google.com/ac/apps/cs/diagnostic>

```bash 
_mta-sts v=STSv1;id=1577377920599;
_smtp._tls v=TLSRPTv1;rua=mailto:reports@willeke.com;
```

## Policy file

<https://mta-sts.willeke.com/.well-known/mta-sts.txt>
Content should be:version: STSv1
mode: testing
mx: aspmx.l.google.com
mx: alt1.aspmx.l.google.com
mx: alt2.aspmx.l.google.com
mx: alt3.aspmx.l.google.com
mx: alt4.aspmx.l.google.com
max_age: 604800
