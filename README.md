# Postgres

Don't forget to install the SSL certification.

## SSL

Run:

```bash
openssl req -new -text -passout pass:abcd -subj /CN=localhost -out postgres/cert/server.req -keyout postgres/cert/privkey.pem \
&& openssl rsa -in postgres/cert/privkey.pem -passin pass:abcd -out postgres/cert/server.key \
&& openssl req -x509 -in postgres/cert/server.req -text -key postgres/cert/server.key -out postgres/cert/server.crt \
&& chmod 600 postgres/cert/privkey.pem postgres/cert/server.crt postgres/cert/server.key postgres/cert/server.req
```
