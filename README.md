# PawMeet 法律文档（唯一正文源）

只改这两个文件：

- `privacy-policy.html`
- `service-agreement.html`

改完执行 **一条命令**：

```powershell
powershell -ExecutionPolicy Bypass -File docs/github-pages/update-legal.ps1
```

会同步进 App 的 `static/legal/`。重新打包后应用内即是最新全文。

若还要更新华为 AGC / 商店填的公网地址，加上 `-Publish`：

```powershell
powershell -ExecutionPolicy Bypass -File docs/github-pages/update-legal.ps1 -Publish
```

（需能登录 GitHub；`publish.ps1` 会先同步再推送。）

---

| 用途 | 读哪里 |
| --- | --- |
| App 内协议页 / 原生弹窗链接 | `static/legal/*.html`（由上面命令生成） |
| 商店提交 URL | https://shaoliangluo.github.io/pawmeet-legal/privacy-policy.html |

同意弹窗里的短摘要不是正文，点链接仍打开同一份全文。
