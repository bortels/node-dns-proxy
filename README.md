node-dns-proxy
==============

A simple DNS proxy server for Node.js

## Installation

``` shell
npm install dnsproxy
sudo node test.js
```

Statement of intent:

We use Infoblox to serve DNS - but Infoblox doesn't do SSHFP records. Rather than wait for them, my goal is
to use a proxy to detect requests for SSHFP records and change it to a TXT request - then take the TXT response
and reformat them as proper SSHFP records. This will let me populate Infoblox with the key hash signatures as
TXT records, and we win. I'd have just done this on the F5 but the licensing is restrictive. 
