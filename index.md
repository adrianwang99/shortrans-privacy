# Shortrans 隐私政策

最后更新：2026-10-05 · Last updated: 2026-10-05

## 概述

Shortrans 不收集、不上传、不出售你的任何个人数据，开发者也不运营任何接收你数据的服务器。

Shortrans 是一款浏览器扩展，用你自己提供的 AI API Key（例如 DeepSeek）翻译网页、EPUB 和 PDF。翻译请求由你的浏览器直接发往你配置的 API 服务商，不经过开发者。本政策适用于 Shortrans 的 Chrome 版和 Safari 版。

## 我们处理哪些数据

下列数据只存在你自己的设备上，或者只发送给你自己配置的 API 服务商。

| 数据 | 用途 | 存在哪里 | 是否离开你的设备 |
| --- | --- | --- | --- |
| API Key、API 地址、模型名 | 调用你选择的翻译服务 | 扩展本地存储 | API Key 只作为请求头发给你配置的 API 地址 |
| 其他设置（目标语言、界面语言、快捷键） | 记住你的偏好 | 扩展本地存储 | 否 |
| 你触发翻译的网页文字、输入框文字 | 生成译文 | 不保存 | 是，发给你配置的 API 服务商 |
| 你打开的 EPUB / PDF 文件及其译文 | 整本翻译、断点续译、阅读 | 浏览器本地数据库（IndexedDB） | 文件本身不上传；其中的文字会分段发给你配置的 API 服务商 |
| 扫描版 PDF 的页面图像 | 本地 OCR 识别文字 | 不单独保存 | 否，OCR 引擎和语言模型都打包在扩展内 |

Shortrans 不收集姓名、邮箱、浏览记录、位置或设备标识。只有在你主动触发翻译时，对应的文字才会被发送。

## 数据如何传输

待翻译的文字只会发送到你在设置里填写的 API 地址，默认是 `https://api.deepseek.com/chat/completions`。

- 请求通过 HTTPS 从你的浏览器直接发出，开发者无法看到请求内容、译文或你的 API Key。
- 收到这些数据的 API 服务商按它自己的隐私政策和服务条款处理数据，例如是否留存、是否用于训练。请在使用前阅读你所选服务商的政策。
- 不要在包含密码、证件号码等敏感信息的页面上触发翻译，除非你信任自己选择的服务商。

## 本地存储与删除

所有数据都由你自己控制，卸载扩展即可全部清除。

- 设置和 API Key 存在浏览器为扩展提供的本地存储中，不会通过浏览器账号同步到其他设备。
- EPUB / PDF 翻译任务、原文件和译文存在本地 IndexedDB 中。在阅读器的任务列表里点「删除」，就会删除该任务的全部数据。
- 在设置页清空 API Key，即可删除已保存的 Key。
- 卸载扩展（Safari 版为删除 App）时，浏览器会删除以上所有数据。

## 权限说明

每个权限都只用于翻译功能本身。

| 权限 | 用途 |
| --- | --- |
| 访问所有网站（`<all_urls>`） | 在你浏览的任意网页上插入译文，并向你自定义的 API 地址发送请求 |
| `storage`、`unlimitedStorage` | 保存设置，以及体积较大的 EPUB / PDF 和译文 |
| `tabs`、`scripting` | 安装或更新后，把翻译脚本注入到已经打开的标签页 |
| `offscreen` | 在后台运行文档翻译任务，关闭阅读页后也能继续 |
| `alarms` | 浏览器重启后恢复未完成的文档翻译任务 |

## 我们不做的事

- 不出售、不出租、不共享你的数据。
- 不使用任何分析、追踪、崩溃上报或广告 SDK。
- 不将数据用于与翻译无关的用途，也不用于评估信用或发放贷款。
- 不加载或执行远程代码，所有脚本、PDF 解析库和 OCR 模型都随扩展一起打包。

Shortrans 对用户数据的使用遵守 [Chrome 应用商店用户数据政策](https://developer.chrome.com/docs/webstore/program-policies/user-data-faq)，包括其中的「有限使用」（Limited Use）要求。

## 儿童隐私

Shortrans 不面向 13 岁以下儿童，也不会有意收集儿童的个人信息。

## 政策变更

本政策如有更新，会发布在本页面并修改顶部的「最后更新」日期。如果改动涉及数据处理方式（例如以后加入付费功能或账号系统），会在扩展更新说明中提示。

## 联系方式

对本政策有任何问题，请发邮件至 wang1118911@gmail.com。

## English Version

**Shortrans does not collect, upload or sell any personal data, and the developer runs no server that receives your data.**

Shortrans is a browser extension that translates web pages, EPUB and PDF files using an AI API key you provide (for example, DeepSeek). Translation requests go directly from your browser to the API provider you configure, never through the developer. This policy covers both the Chrome and Safari versions.

**Data we handle**

| Data | Purpose | Where it is stored | Leaves your device? |
| --- | --- | --- | --- |
| API key, API URL, model name | Call the translation service you chose | Extension local storage | The key is sent only as a request header to your configured API URL |
| Other settings (target language, UI language, shortcuts) | Remember your preferences | Extension local storage | No |
| Page or input text you ask to translate | Produce the translation | Not stored | Yes, to your configured API provider |
| EPUB / PDF files you open, and their translations | Book translation, resume, reading | Local IndexedDB | The file is not uploaded; its text is sent in chunks to your configured API provider |
| Page images of scanned PDFs | Local OCR | Not stored separately | No; the OCR engine and language models are bundled |

Shortrans does not collect names, email addresses, browsing history, location or device identifiers. Text is sent only when you trigger a translation.

**How data is transmitted.** Text is sent over HTTPS only to the API URL in your settings (default `https://api.deepseek.com/chat/completions`). The developer cannot see your requests, translations or API key. Your API provider handles the data under its own privacy policy and terms, so please review them.

**Storage and deletion.** Settings stay in the extension's local storage and are not synced. Document jobs are kept in local IndexedDB; deleting a job in the reader removes all its data. Uninstalling the extension (or deleting the Safari app) removes everything.

**Permissions.** Access to all sites: insert translations on any page and reach your custom API URL. `storage` / `unlimitedStorage`: save settings and large documents. `tabs` / `scripting`: inject the translator into already-open tabs after install or update. `offscreen`: run document translation in the background. `alarms`: resume unfinished jobs after a browser restart.

**What we don't do.** No selling or sharing of data; no analytics, tracking, crash reporting or ad SDKs; no use for unrelated purposes, credit or lending; no remote code. Use of user data complies with the [Chrome Web Store User Data Policy](https://developer.chrome.com/docs/webstore/program-policies/user-data-faq), including the Limited Use requirements.

**Children.** Shortrans is not directed at children under 13 and does not knowingly collect their data.

**Changes.** Updates will be posted on this page with a new "Last updated" date; changes to data handling will be noted in the extension's release notes.

**Contact.** wang1118911@gmail.com
