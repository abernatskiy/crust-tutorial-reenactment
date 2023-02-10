Steps to reproduce the http 500 error on crust arhive:
```bash
git clone https://github.com/abernatskiy/crust-tutorial-reenactment
cd crust-tutorial-reenactment
npm ci
sqd build
nano +200 node_modules/@subsquid/util-internal-http-client/lib/client.js
(apply the changes proposed by this commit)
sqd process
```
Occurs after block 688000
