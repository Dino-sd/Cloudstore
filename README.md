# Cloudstone

[MITM]
hostname = api.revenuecat.com

[Script]
Locket Gold = type=http-response, pattern=^https:\/\/api\.revenuecat\.com\/.+\/(receipts$|subscribers\/[^/]+$), requires-body=1, max-size=0, script-path=https://raw.githubusercontent.com/Dino-sd/Cloudstore/refs/heads/Module/Locket.js, update-interval=5

[Header Rewrite]
^https?://api.revenuecat.com/.+/(receipts$|subscribers/?(.*?)*$) = delete header X-RevenueCat-ETag
^https?://api.revenuecat.com/.+/(receipts$|subscribers/?(.*?)*$) = delete header x-revenuecat-etag
