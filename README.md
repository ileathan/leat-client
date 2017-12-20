# leat-client
Javascript client side miner wrapper.

`leat-mine.js` Is the main file that should be served via

```html
<script src="yourdomain.com/leat-mine.js"></script>
<script>
new leatMine().start();
</script>
```

Then you edit the bottom of `leat-mine.js` file.

# Full instalation

1.) Install and run `leat-stratum-proxy`

2.) copy `https://leat.io/lib/leat-mine.js` (this repo) and `https://leat.io/lib/leathash.wasm` and `https://leat.io/lib/leathash-amjs.min.js` files into your local webserver.

3.) Open `leat-mine.js` and scroll to the bottom. edit

```
  LIB_URL: 'https://leat.io/lib/',
  ASMJS_NAME: 'leathash-asmjs.min.js',
  REQUIRES_AUTH: false,
  WEBSOCKET_SHARDS: [['wss://leat.io']],
  CAPTCHA_URL: '',
  MINER_URL: '',
  AUTH_URL: ''
```

lines accordingly. Also make sure to edit the same things in the big fat long last line.

**Thats it!**
