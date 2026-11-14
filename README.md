# audio-converter-config

Public, no-secrets config for the 音乐格式转换器 Windows client.

The app reads `config.json` at startup (and again if a shop request fails) so a temporary tunnel can change URL without rebuilding the exe.

```json
{ "shop_url": "https://example.free.pinggy.net" }
```

Lookup order in the app: `AUDIOCONV_SHOP_URL` → this file on GitHub raw → jsDelivr → last cached URL → baked default.

Do not put passwords, private keys, or `.env` files in this repository.
