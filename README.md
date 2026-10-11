<div align="center">

# 🦁 XXD Shop 009｜高转化主视觉

### 信息再多，第一眼也永远知道该看哪里

<strong>简体中文</strong> · <a href="README.en.md">English</a>

</div>

> 原始提示词：[简体中文原文](references/original-prompt/zh-CN.md) · [English](references/original-prompt/en.md)

## 样张

暂无样张。下文命令只是用法示例，不是视觉证据。

## 它解决什么

大促主图最容易做成这样：五个卖点都高亮，三种红黄绿抢着出现，价格和卖点挤成一团，顾客找不到入口。

**Shop 009** 按原稿的顺序做减法和组织：

1. **先定这一张的任务**：品牌感、核心卖点、价格优势、食欲、新鲜、品质还是礼赠。整张只有一个最强信息中心。
2. **商品是真的、有重量的主体**，周围保持干净，装饰不穿过轮廓。
3. **颜色先保护商品**，再决定环境；全图只留少量真正有攻击力的强调色。
4. **文字成组**：身份与标题、核心利益、辅助卖点、价格与购买、产地规格成分工艺，靠字号、留白和位置区分，不靠堆颜色。
5. **价格的分量看商品**：高频促销品可以把价格做成锚点，高端礼赠品让品牌先出场。

## 你需要准备

- **商品图或商品名称。**
- **卖点：** 一段文案就够，用 `--text plan --copy` 交给它提炼分组。
- **事实：** 价格、原价、优惠时间、规格、产地、成分。没给价格，画面就没有价格组，不会出现占位价。

## 001 还是 009？

| | 001 高级商业主视觉 | 009 高转化主视觉 |
|---|---|---|
| 气质 | 安静、留白、品牌感 | 转化导向、信息有层级 |
| 文字 | 标题可有可无 | 图文混排是核心 |
| 价格 | 通常不出现 | 可以是视觉锚点 |

## 开始使用

```bash
git clone https://github.com/nevertoday/xxd-shop-009.git
ln -s "$(pwd)/xxd-shop-009" ~/.claude/skills/xxd-shop-009
```

```text
# 大促价格图：价格放在文案方案最前面，卖点交给它提炼，价格和时间由你提供
/xxd-shop-009 ./空气炸锅.png --use 电商主图 --focus "主打价格优势" --size 1:1 \
  --text plan --copy "到手价 ¥299 原价 ¥459 6L 大容量 一锅出全家菜 可视窗口 免翻面 少油健康" \
  --facts "到手价 ¥299，原价 ¥459；11.1–11.11；容量 6L" --locale zh-CN

# 高端礼赠：品牌先出场，价格不叫卖
/xxd-shop-009 ./茶叶礼盒.png --use 详情页首屏 --focus "主打中秋礼赠价值" --size 3:4 --text prompt --facts "武夷山正岩产区；250g×2 罐" --locale zh-CN

# 没有价格：画面不会出现价格组
/xxd-shop-009 ./洗地机.png --size 1:1 --text plan --copy "吸拖洗烘一体 贴边清洁 自清洁" --locale zh-CN
```

想让价格压过卖点，把价格写在文案方案的第一句。原稿要求大标题本身有足够视觉重量，方案排在最前的句子最容易被当成主标题；只写 `--focus` 时，价格往往是醒目的第二中心。

常用参数：`--focus` 本张任务 · `--use` 用途 · `--text plan` + `--copy` · `--facts` · `--size` · `--count` · `--locale`。完整参数见[家族运行合同](references/shop-runtime.md)。

## 边界与信任

- 原始提示词逐字保存，是唯一的审美权威。
- 画面上的每一个数字（价格、折扣、时间、规格）都能在你给的事实里找到。
- 交付 PNG 位图；每次调用都新建任务目录。

<!-- xxd-shop-tail -->
## 项目结构

```text
xxd-shop-009/
├── SKILL.md
├── README.md / README.en.md
├── LICENSE
├── agents/openai.yaml
├── assets/examples/
├── scripts/
│   ├── configured_imagegen.py
│   └── shop_preferences.py
└── references/
    ├── shop-runtime.md
    ├── runtime-preferences.md
    ├── sample-workflow.md
    └── original-prompt/
        ├── README.md
        ├── zh-CN.md
        └── en.md
```

<!-- xxd-readme-ads:start -->
## 关于 XXD

XXD 是小小东品牌名的缩写，本项目由小小东创建并维护：[@xiaoxiaodong01](https://x.com/xiaoxiaodong01)。

## 小小东多端会员 · 699 元/年

> **广告与商业信息声明：** 以下二维码、会员与付费服务链接属于小小东的广告信息。是否扫码或购买完全自愿，不影响本开源项目的访问与使用。

一次年费，同时开通三项会员权益：**知识星球 + 小小东成员提示词库 + 全部 将军总指挥 Skills 会员**。三项权益合并在同一份会员中，无需分别购买。

<!-- xxd-shop-command-system:start -->

### Skills 如何协作

| 层级 | 包含内容 | 用途 |
|---|---|---|
| **General** | `xxd-shop-all` | 识别可用的编号 Skills，按商品、用途和画面需求推荐，并组织多风格试稿与批量任务。 |
| **Soldier** | `xxd-shop-NNN` | 每个编号执行自己的原始提示词与审美，完成 General 分派的具体任务。 |

<!-- xxd-shop-command-system:end -->

### 会员权益

1. **微信一对一 AI 学习与项目答疑**
   扫描下方二维码，添加小小东微信，围绕 AI 学习、工具使用和实际项目进行一对一沟通，获得答疑与建议；代表性问题将整理为会员内容。
2. **持续更新的成员提示词库**
   [小小东成员提示词库](https://vip.xiaoxiaodong.ai/)当前约有 3.2 万条提示词，会持续整理和扩充，目标超过 10 万条。
3. **全部 将军总指挥 Skills 与使用答疑**
   一份会员覆盖全部 将军总指挥 Skills；使用过程中遇到问题，可以获得相应的使用说明与答疑。
4. **高频刚需优先处理**
   会员提出的高频、刚需提示词与 Skills 需求，会优先评估和开发。

### 如何开通

- 可在[成员网站](https://vip.xiaoxiaodong.ai/)自助开通。
- 也可以扫描下方二维码，添加小小东微信，进行一对一沟通并获得开通协助。

<p align="center"><a href="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png"><img src="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png" alt="联系小小东" width="280"></a></p>
<!-- xxd-readme-ads:end -->

## 许可证

本项目（包括 Skill、提示词、脚本、文档及随附样张）采用 **PolyForm Noncommercial License 1.0.0**。完整法律条文请见 [LICENSE](LICENSE)，官方页面见 <https://polyformproject.org/licenses/noncommercial/1.0.0>。

用人话说：

- 个人可以用于学习、研究、实验、测试、兴趣项目和私人娱乐；慈善机构、教育机构、公共研究/安全/卫生机构、环保组织及政府机构也可以使用。
- 在**非商业目的**下，你可以使用、复制、修改、制作衍生作品并分享；分享时必须同时提供本许可证（或上面的链接）以及作者提供的所有 `Required Notice:` 声明。
- 不允许用于商业产品或服务、收费交付、出售访问权或许可，或任何预期会带来商业应用的用途。需要商业使用时，请先向版权方另行取得书面许可。
- 本协议只授予其中明确写出的著作权许可和有限的专利许可，不授予商标、品牌名称或其他未明确授予的权利，也不能把你的许可再转授给他人。
- 如果收到书面违约通知，须在 32 天内纠正并采取实际补救措施，否则许可会立即终止；就专利侵权提出书面主张也会终止专利许可。
- 内容按“现状”提供，在法律允许的范围内不作任何担保，使用风险和可能的损失由使用者自行承担。
