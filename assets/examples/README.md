# XXD Shop 009 样张

每张都是本编号按 `references/sample-workflow.md` 一次生成、目视通过的原图，像素未改，只清理了元数据。商品是虚构的演示品牌，画面上的价格、规格等数字都是演示设定。

| 文件 | 用途 | 实际像素 | 输入 | 文字方式 | visual_review |
|---|---|---|---|---|---|
| `c01-category-1x1-1254x1254.png` | 大促主图 | 1254x1254 | 商品图 `product-xunyu-shoe.jpg`、Logo `logo-xunyu.png` | plan zh-CN | passed |
| `c02-category-1x1-1254x1254.png` | 大促主图 | 1254x1254 | 商品图 `product-xxg-diaper.jpg`、Logo `logo-xiaoxiangguo.png` | plan zh-CN | passed |
| `c03-category-3x4-1086x1448.png` | 3:4 主图 | 1086x1448 | 商品图 `product-mqx-catfood.jpg`、Logo `logo-maoqiuxing.png` | plan zh-CN | passed |
| `c04-category-1x1-1254x1254.png` | 大促主图 | 1254x1254 | 商品图 `product-qy-laundry.jpg`、Logo `logo-qingyu.png` | plan zh-CN | passed |
| `c05-category-16x9-1672x941.png` | 活动横幅 | 1672x941 | 商品图 `product-nuandao-robot.jpg`、Logo `logo-nuandao.png` | plan zh-CN | passed |
| `c06-category-1x1-1254x1254.png` | 大促主图 | 1254x1254 | Logo `logo-chengli.png` | plan zh-CN | passed |
| `p01-set-1x1-1254x1254.png` | 主图五连 | 1254x1254 | 商品图 `product-nuandao-fryer.jpg`、Logo `logo-nuandao.png` | plan zh-CN | passed |
| `p02-set-1x1-1254x1254.png` | 主图五连 | 1254x1254 | 商品图 `product-nuandao-fryer.jpg`、Logo `logo-nuandao.png` | exact zh-CN | passed |
| `p03-set-1x1-1254x1254.png` | 主图五连 | 1254x1254 | 商品图 `product-nuandao-fryer.jpg`、Logo `logo-nuandao.png` | plan zh-CN | passed |
| `p04-set-1x1-1254x1254.png` | 主图五连 | 1254x1254 | 商品图 `product-nuandao-fryer.jpg`、Logo `logo-nuandao.png` | plan zh-CN | passed |
| `s01-size-1x1-1254x1254.png` | 大促主图 | 1254x1254 | 商品图 `product-nuandao-fryer.jpg`、Logo `logo-nuandao.png` | plan zh-CN | passed |
| `s02-size-3x4-1086x1448.png` | 3:4 主图 | 1086x1448 | 商品图 `product-nuandao-fryer.jpg`、Logo `logo-nuandao.png` | plan zh-CN | passed |
| `s03-size-9x16-941x1672.png` | 开屏 | 941x1672 | 商品图 `product-nuandao-fryer.jpg`、Logo `logo-nuandao.png` | plan zh-CN | passed |
| `s04-size-16x9-1672x941.png` | 活动横幅 | 1672x941 | 商品图 `product-nuandao-fryer.jpg`、Logo `logo-nuandao.png` | plan zh-CN | passed |
| `s09-special-1x1-1254x1254.png` | 大促主图 | 1254x1254 | 原图 `orange.jpg`、Logo `logo-chengli.png` | plan zh-CN | passed |
| `s10-special-1x1-1254x1254.png` | 礼赠主图 | 1254x1254 | 商品图 `product-yunao-giftbox.jpg`、Logo `logo-yunao.png` | plan zh-CN | passed |
| `s11-special-1x1-1254x1254.png` | 跨境主图 | 1254x1254 | 商品图 `product-nuandao-dryer-red.jpg`、Logo `logo-nuandao.png` | plan en-US | passed |

## 输入素材

`sources/` 里是生成时交给本编号的输入缩样，模拟商家手里的素材：带包装与 Logo 的商品图、品牌 Logo，个别为原图。
演示品牌、Logo 和商品图由本项目生成；其中以 Unsplash 照片为底的，署名如下，适用 [Unsplash License](https://unsplash.com/license)，**不属于**本仓库的 PolyForm Noncommercial 授权范围。

| 输入 | 说明 · 来源 |
|---|---|
| `sources/logo-chengli.png` | 演示品牌 Logo，本项目生成 |
| `sources/logo-maoqiuxing.png` | 演示品牌 Logo，本项目生成 |
| `sources/logo-nuandao.png` | 演示品牌 Logo，本项目生成 |
| `sources/logo-qingyu.png` | 演示品牌 Logo，本项目生成 |
| `sources/logo-xiaoxiangguo.png` | 演示品牌 Logo，本项目生成 |
| `sources/logo-xunyu.png` | 演示品牌 Logo，本项目生成 |
| `sources/logo-yunao.png` | 演示品牌 Logo，本项目生成 |
| `sources/orange.jpg` | 原图 [vRF8YpnkSHc](https://unsplash.com/photos/vRF8YpnkSHc) · @fukayamamo |
| `sources/product-mqx-catfood.jpg` | 演示商品图，本项目生成 |
| `sources/product-nuandao-dryer-red.jpg` | 演示商品图，本项目生成；底图 [a5Ekb8Q3q-0](https://unsplash.com/photos/a5Ekb8Q3q-0) · @theshubhamdhage |
| `sources/product-nuandao-fryer.jpg` | 演示商品图，本项目生成 |
| `sources/product-nuandao-robot.jpg` | 演示商品图，本项目生成 |
| `sources/product-qy-laundry.jpg` | 演示商品图，本项目生成 |
| `sources/product-xunyu-shoe.jpg` | 演示商品图，本项目生成 |
| `sources/product-xxg-diaper.jpg` | 演示商品图，本项目生成 |
| `sources/product-yunao-giftbox.jpg` | 演示商品图，本项目生成 |
