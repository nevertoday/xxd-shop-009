---
name: xxd-shop-009
description: "Create XXD Shop 009 high-conversion brand main visuals (高转化电商主视觉) as finished PNGs from a product photo, product directory or product name plus selling points and facts, treating the bundled original brief as the sole aesthetic authority: one strongest information centre per image, a real product with weight and footing, colour that protects the product first, a large title that is also a visual shape, copy grouped into identity, core benefit, secondary benefits, price-offer and proof clusters, and a price whose presence depends on the product's positioning. Supports multiple ratios or exact sizes, several compositions per size, prompt-generated, user-exact or user-plan copy, and supplied facts only. Use when the user invokes xxd-shop-009 or asks for 高转化主图、带价格的主图、卖点主图、大促主图、活动主图、图文混排主视觉."
---

# XXD Shop 009｜高转化主视觉

用本次的商品图或商品名称，加上卖点、价格与证明信息，生成一张“第一眼永远知道该看哪里”的高转化电商主视觉，交付 PNG。

每次生成前，完整读取 `references/original-prompt/zh-CN.md`。这份中文原始提示词是唯一的创作与审美权威；不总结、不翻译、不混用，也不用本文件、README、样张或其他编号替代它。

每次构建生图请求前，完整读取 `references/shop-runtime.md`，它是唯一的家族运行合同。本 Skill 不另写第二套美术指导或运行规则。

所有成品直接写进 `~/Desktop/xxd/xxd-shop-009/` 下新建的一个任务目录（或 `--out` 指定的根目录），不建子目录，不自动拼总览。

## 本编号覆盖条款

**“这张图最重要的任务”由谁定。** 原稿要求先判断任务：品牌感、核心卖点、价格优势、食欲、新鲜感、品质感或礼赠价值，并且整张只允许一个最强信息中心。用户用 `--focus` 或描述说了任务（例如 `--focus "主打价格优势"`、“这张主打礼赠”），原话写进商品块的“本张重点”行，对应原稿概念写作「这一张图最重要的任务，也是全图唯一最强的信息中心」；用户没说，交给图像模型按原稿判断，外层不替用户选。

实测中，方案的第一句最容易被当成原稿要求有“足够视觉重量”的大标题。所以本张重点是价格、方案却不以价格开头时，生成前用一句话提醒用户：可以把价格写进方案第一句。用户不改就照原样执行；外层既不替用户调换顺序，也不另加“放大价格”之类的美术指令。

**信息分组需要真材料。** 原稿把文字分成五组：产品身份与主标题、核心利益点、辅助卖点、价格优惠与购买信息、产地规格成分工艺等证明信息。

- 价格、优惠、时间、产地、规格、成分、工艺都是事实，只来自“可用事实”。
- 没有价格时，画面就没有价格组，不放占位价格，也不写“限时特惠”这类没有依据的促销；原稿“价格有独立识别”的要求只在有价格时适用。
- 用户有一段卖点文案时，推荐 `--text plan --copy "..."`：原稿本来就要求“卖点优先提炼，不机械罗列”，方案模式让模型按五组理顺，不改意思、不加事实。

**“不要文字”与原稿冲突。** 原稿的核心是“文字与商品真正混排”。`--text none` 时说明这会去掉原稿的大半，用户坚持才执行。

**与 001 的区别**（帮用户选对编号时说明）：001 安静高级，标题可有可无；009 是转化导向的图文系统，信息更多、价格可以是锚点。

**追加验收：** 只有一个最强信息中心；同类信息成组，不是满屏散落的标签；价格数字优先于单位、原价、优惠说明和时间；装饰和纹理没有穿过商品轮廓；没有九宫格式机械排版；画面上的每一个数字都能在事实里找到。

## 参考文件

- `references/shop-runtime.md`：家族运行合同
- `references/original-prompt/zh-CN.md`：运行时使用的原始提示词
- `references/original-prompt/README.md`：译文索引与权威说明
- `references/runtime-preferences.md`：交付偏好沿用
- `references/sample-workflow.md`：仅用于维护样张
- `scripts/configured_imagegen.py`、`scripts/shop_preferences.py`
