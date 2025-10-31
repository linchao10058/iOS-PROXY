// Surge Script: Remove Startup Ads from multiple apps
// Author: linchao10058
// Updated: 2025-03-27

let body = $response.body;

if (!body) {
  $done({});
  return;
}

try {
  let obj = JSON.parse(body);

  // 12306
  if (obj.datas) obj.datas = [];

  // 京东
  if (obj.data) obj.data = [];
  if (obj.ads) obj.ads = [];

  // B站
  if (obj.data) obj.data = [];

  // 微信
  if (obj.advertisement_info) obj.advertisement_info = [];
  if (obj.advertisement_num) obj.advertisement_num = 0;

  // 微博
  if (obj.data) obj.data = [];

  // 小红书
  if (obj.data && obj.data.ads) obj.data.ads = [];

  // 顺丰
  if (obj.data) obj.data = [];

  // 通用字段
  if (obj.ad) obj.ad = null;
  if (obj.advert) obj.advert = null;
  if (obj.startup) obj.startup = null;

  $done({ body: JSON.stringify(obj) });
} catch (e) {
  $done({ body: "{}" });

[Script]
Startup_Ads_Blocker = type=http-response, pattern=^https?:\/\/.*(splash|ad|advert|startup), requires-body=1, max-size=524288, script-path=local-path-to/Advertising.js

}
