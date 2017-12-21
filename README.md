# leat-client
Javascript client side miner wrapper.

`leat-mine.js` Is the main file that should be served via

# Usage 

```html
<script src="yourdomain.com/leat-mine.js"></script>
<script>
new leatMine().start();
</script>
```

Or more thorough usage:

```html
<script src="/leat-mine.js"></script>
<script>
leatMine.CONFIG = {
  LIB_URL: 'https://leat.io/lib/',
  ASMJS_NAME: 'leathash-asmjs.min.js',
  REQUIRES_AUTH: false,
  WEBSOCKET_SHARDS: [['wss://leat.io']],
  CAPTCHA_URL: '',
  MINER_URL: 'https://leat.io/m.html',
  AUTH_URL: ''
};

const leatMiner = new leatMine.User(ADDRESS, USERNAME/*, OPTIONS*/)

leatMiner.start();
</script>
```

Then you edit the bottom of `leat-mine.js` file.

# Full installation

1.) Install and run [leat-stratum-proxy](https://github.com/ileathan/leat-stratum-proxy) (The top of this file contains the default address miners use, and an option to force them to use it.) **This step + serving the client with `leat-mine.js` is all thats needed**

2.) For best preformance host `https://leat.io/lib/leat-mine.js` (this repo) `https://leat.io/lib/leathash.wasm`, `https://leat.io/lib/leathash-amjs.min.js` and `https://leat.io/lib/leathash-amjs.min.js.mem` locally on your webserver.

3.) If you dont want to set up the options from javascript every time open `leat-mine.js` and scroll to the bottom. edit the following lines according to where you hosted the files.

```
  LIB_URL: 'https://leat.io/lib/',
  ASMJS_NAME: 'leathash-asmjs.min.js',
  REQUIRES_AUTH: false,
  WEBSOCKET_SHARDS: [['wss://leat.io']],
  CAPTCHA_URL: '',
  MINER_URL: 'https://leat.io/m.html',
  AUTH_URL: ''
```

Also make sure to edit the same things in the big fat long last line.
