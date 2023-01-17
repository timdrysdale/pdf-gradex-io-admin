# pdf-gradex-io-admin
Blog admin commands

## SSL certs 

Check the certificate start/end dates

```
echo  | openssl s_client -servername pdf.gradex.io -connect pdf.gradex.io:443 | openssl x509 -noout -dates
```

upgrade:
```
sudo certbot certonly --manual -d '*.gradex.io'

```

Modify the acme_challenge in the Advanced DNS page at the registry.

```
sudo nginx -t #check config ok
sudo systemctl restart nginx
```

Check the certificate start/end dates

```
echo  | openssl s_client -servername pdf.gradex.io -connect pdf.gradex.io:443 | openssl x509 -noout -dates
```
