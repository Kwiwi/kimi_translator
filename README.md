<details>
<summary>中文版</summary>

两个功能：多语翻译 和 语法纠错，详见下文。
Moonshot API+Cloudflare Pages实现的。
我认为最重要的是可以直接写提示词要求怎么翻译/着重检查什么语法。
~~虽然说和自己打开Kimi app问没多大区别~~ 

---

`05/30/2026更新：增加了流式输出和优化了语法纠错过于苛刻的问题`

---

### 功能

- 翻译：默认中译英，翻译成其他语言需要自己在自定义要求那里指定。预设有三种语气：随意 / 自然 / 正式 
- 语法纠错：修正语法和拼写，同时保留原有语气与风格。也可以指定要求。

还有双语界面、夜间模式、响应式界面、流式输出什么的

</details>

---

Two main features: multilingual translation and grammar correction. Check the details below.

Built using Moonshot API and Cloudflare Pages.

I think the key thing is you can just write prompts to specify exactly how you want things translated or what grammar to focus on.

~~Though it’s not that different from just opening the Kimi app and asking~~

---

`May 30, 2026 update: Added streaming output and fixed the grammar checker—it was getting way too picky.`

---

### Features

Translation: It defaults to Chinese-to-English, but you can specify other languages in the custom settings if you want. There are three preset tones to pick from: casual, natural, and formal.

Grammar Check: Fixes up grammar and spelling while keeping the original tone and style. You can also throw in specific requests if you need.

And there's bilingual interface, dark mode, responsive design, streaming output,etc.

---

### Screenshots/页面截图

| ☀️ | 🌙 |
|:-----------:|:-----------:|
| ![☀️](screenshot_light.jpg) | ![🌙](screenshot_dark.jpg) |

---

Personal hobby project by a high schooler. There may be some bugs.

高中生个人小项目，可能有 bug。

---

### License

MIT License
MIT协议

---

### Credits/鸣谢
Kimi K2.6 + K2.5
GPT-5.5
Claude Sonnet 4.6

---
<details>
<summary>deployment guide/部署指南</summary>

`Written by Kimi—I didn't feel like editing it`
`A deployment guide by Kimi, written specifically for beginners`

`Kimi写的——我懒得改了`
`Kimi写的部署指南，专门给新手看的`


## 技术栈 / Tech Stack

| 层级 / Layer | 技术 / Technology |
|:---:|:---:|
| 前端 / Frontend | Vanilla HTML + CSS + JS |
| 后端 / Backend | Cloudflare Pages `_worker.js` |
| AI 接口 / AI API | Moonshot Kimi API (`kimi-k2.5`) |


## 部署 / Deployment

### 1. 准备文件 / Prepare Files

```
your-project/
├── _worker.js        # 后端 API 代理 / Backend API proxy
├── translator.html   # 前端界面 / Frontend interface
└── index.html        # 现有主页（可选）/ Your existing homepage (optional)
```

### 2. 上传到 Cloudflare Pages / Upload to Cloudflare Pages

1. 打开 [Cloudflare Dashboard](https://dash.cloudflare.com) → Pages → Create a project
2. **上传文件** / **Upload your files**（拖拽上传 / drag & drop）
3. 点击部署 / Deploy

### 3. 设置环境变量 / Set Environment Variables

Pages Project → Settings → Environment variables:

| 变量 / Variable | 值 / Value |
|:---:|:---:|
| `KIMI_API_KEY` | 你的 Moonshot API 密钥，以 `sk-`  开头 / Your Moonshot API key (starts with `sk-`) |

### 4. 设置兼容性日期 / Set Compatibility Date

Pages Project → Settings → Functions → Compatibility date:

- 生产环境 / Production: `2026-05-14`（或最新可用日期 / or latest available）

保存后重新部署 / Save and redeploy.

### 5. 访问 / Visit

```
https://your-project.pages.dev/translator.html
```

---

## 本地测试 / Local Testing

直接用浏览器打开 `translator.html` 即可预览界面（无 `_worker.js` 时后端调用会失败，但 UI 正常显示）。

Open `translator.html` directly in browser. Backend calls will fail without `_worker.js`, but the UI works fine.

</details>
