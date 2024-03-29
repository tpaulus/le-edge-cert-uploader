# Let's Encrypt Edge Cert Uploader
A docker container that obtains a certificate from Let's Encrypt for a specified set of domains and then uploads it as a
custom edge certificate to Cloudflare.

**Prerequisites:**

You will need a Cloudflare API Key that is allowed to edit DNS and SSL settings, as well as a Business or Enterprise Zone.

Run via:
```shell
docker run \
  -e DOMAINS=<DOMAIN LIST COMMA SEPARATED> \
  -e CF_ZONE_ID=<CLOUDFLARE ZONE ID> \
  -e CF_API_KEY=<YOUR CLOUDFLARE API KEY> \
  -e EMAIL=<YOUR EMAIL ADDRESS> \
  --pull=always \
  --rm \
  ghcr.io/tpaulus/le-edge-cert-uploader:main
```
