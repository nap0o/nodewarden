# 🛡️ 安全审计与透明度报告

[English](README.md) | 中文

![安全评级](https://img.shields.io/badge/安全评级-B-blue?style=for-the-badge)

> [!IMPORTANT]
> 本报告由 **GitHub Actions** 自动生成。为确保数据主权的绝对透明度，所有核心模块的安全扫描结果均实时公开。

| 📅 审计时间 | 📝 运行 ID | 🛠️ 环境 |
| :--- | :--- | :--- |
| `2026-03-10 03:36:47 UTC` | [#22885869134](https://github.com/nap0o/nodewarden/actions/runs/22885869134) | `GitHub CI/CD` |

---

## 📉 实时安全仪表盘

| 工具 | 状态 | 发现项 |
| :--- | :--- | :--- |
| **Credential Leak (Gitleaks)** | ![Pass](https://img.shields.io/badge/Status-PASS-success?style=for-the-badge) | `0` 泄露 |
| **Dependency Scan (Snyk)** | ![Pass](https://img.shields.io/badge/Status-PASS-success?style=for-the-badge) | `0` 漏洞 |
| **Static Analysis (CodeQL)** | ![Warning](https://img.shields.io/badge/Status-NOTICE-orange?style=for-the-badge) | `9` 告警 |
| **Container Scan (Trivy)** | ![Pass](https://img.shields.io/badge/Status-PASS-success?style=for-the-badge) | `0` 发现项 |

---

## 🔍 扫描覆盖范围

| 模块 | 已审计文件 | 覆盖率 |
| :--- | :---: | :---: |
| **GitHub Actions** | `2` | ✨ **100%** |
| **JavaScript (Frontend)** | `0` | ✨ **100%** |
| **TypeScript (Backend)** | `40` | ✨ **100%** |

---

## 🔍 详细发现项

### 🔑 凭据泄露检查 (Gitleaks)
`检测代码历史记录中硬编码的 API 密钥、密码或其他敏感令牌。` `扫描范围：所有代码更改和 Git 历史记录 (Gitleaks 全量扫描)`

✅ **安全**：未发现硬编码的敏感凭据。

### 🛡️ 容器配置安全 (Trivy)
`检测 Dockerfile 和容器配置中的安全风险与最佳实践。`

✅ **安全**：未发现容器配置缺陷。

### 📦 第三方依赖
✅ **安全**：在依赖项中未发现已知漏洞。

### 💻 代码质量与安全 (CodeQL)
#### 摘要
- **已检查规则**: `227`
- **告警总数**: `9`

| 规则 ID | 级别 | 位置 | 描述 |
| :--- | :---: | :--- | :--- |
| [js/identity-replacement](https://codeql.github.com/codeql-query-help/javascript/js-identity-replacement/) | 🟠 warning | `webapp/src/App.tsx:1799` | This replaces '/' with itself. |
| [js/clear-text-storage-of-sensitive-data](https://codeql.github.com/codeql-query-help/javascript/js-clear-text-storage-of-sensitive-data/) | 🟠 warning | `webapp/src/components/VaultPage.tsx:534` | This stores sensitive data returned by [a call to computePasswordSignature](1) as clear text. |
| [js/biased-cryptographic-random](https://codeql.github.com/codeql-query-help/javascript/js-biased-cryptographic-random/) | 🟠 warning | `src/utils/recovery-code.ts:15` | Using modulo on a [cryptographically secure random number](1) produces biased results. |
| [js/biased-cryptographic-random](https://codeql.github.com/codeql-query-help/javascript/js-biased-cryptographic-random/) | 🟠 warning | `src/utils/recovery-code.ts:20` | Using modulo on a [cryptographically secure random number](1) produces biased results. |
| [js/biased-cryptographic-random](https://codeql.github.com/codeql-query-help/javascript/js-biased-cryptographic-random/) | 🟠 warning | `webapp/src/components/JwtWarningPage.tsx:80` | Using modulo on a [cryptographically secure random number](1) produces biased results. |
| [js/biased-cryptographic-random](https://codeql.github.com/codeql-query-help/javascript/js-biased-cryptographic-random/) | 🟠 warning | `webapp/src/components/SettingsPage.tsx:21` | Using modulo on a [cryptographically secure random number](1) produces biased results. |
| [js/polynomial-redos](https://codeql.github.com/codeql-query-help/javascript/js-polynomial-redos/) | 🟠 warning | `src/handlers/accounts.ts:49` | This [regular expression](1) that depends on [library input](2) may run slow on strings with many repetitions of '='. |
| [js/unused-local-variable](https://codeql.github.com/codeql-query-help/javascript/js-unused-local-variable/) | 🟠 warning | `webapp/src/lib/export-formats.ts:115` | Unused function toAesBuffer. |
| [js/unused-local-variable](https://codeql.github.com/codeql-query-help/javascript/js-unused-local-variable/) | 🟠 warning | `webapp/src/components/VaultPage.tsx:141` | Unused function fieldTypeLabel. |

### 📂 已审计文件列表
<details>
<summary><b>GitHub Actions (2)</b></summary>

| 模块 | 位置 | 状态 |
| :--- | :--- | :--- |
| `security.yml` | `.github/workflows/security.yml` | ✅ **已审计** |
| `sync-upstream.yml` | `.github/workflows/sync-upstream.yml` | ✅ **已审计** |

</details>

<details>
<summary><b>JavaScript (0)</b></summary>

> 未检索到文件。

</details>

<details>
<summary><b>TypeScript (40)</b></summary>

| 模块 | 位置 | 状态 |
| :--- | :--- | :--- |
| `limits.ts` | `src/config/limits.ts` | ✅ **已审计** |
| `notifications-hub.ts` | `src/durable/notifications-hub.ts` | ✅ **已审计** |
| `accounts.ts` | `src/handlers/accounts.ts` | ✅ **已审计** |
| `admin.ts` | `src/handlers/admin.ts` | ✅ **已审计** |
| `attachments.ts` | `src/handlers/attachments.ts` | ✅ **已审计** |
| `backup.ts` | `src/handlers/backup.ts` | ✅ **已审计** |
| `ciphers.ts` | `src/handlers/ciphers.ts` | ✅ **已审计** |
| `devices.ts` | `src/handlers/devices.ts` | ✅ **已审计** |
| `folders.ts` | `src/handlers/folders.ts` | ✅ **已审计** |
| `identity.ts` | `src/handlers/identity.ts` | ✅ **已审计** |
| `import.ts` | `src/handlers/import.ts` | ✅ **已审计** |
| `notifications.ts` | `src/handlers/notifications.ts` | ✅ **已审计** |
| `sends.ts` | `src/handlers/sends.ts` | ✅ **已审计** |
| `setup.ts` | `src/handlers/setup.ts` | ✅ **已审计** |
| `sync.ts` | `src/handlers/sync.ts` | ✅ **已审计** |
| `index.ts` | `src/index.ts` | ✅ **已审计** |
| `router.ts` | `src/router.ts` | ✅ **已审计** |
| `auth.ts` | `src/services/auth.ts` | ✅ **已审计** |
| `blob-store.ts` | `src/services/blob-store.ts` | ✅ **已审计** |
| `ratelimit.ts` | `src/services/ratelimit.ts` | ✅ **已审计** |
| `storage.ts` | `src/services/storage.ts` | ✅ **已审计** |
| `index.ts` | `src/types/index.ts` | ✅ **已审计** |
| `device.ts` | `src/utils/device.ts` | ✅ **已审计** |
| `jwt.ts` | `src/utils/jwt.ts` | ✅ **已审计** |
| `pagination.ts` | `src/utils/pagination.ts` | ✅ **已审计** |
| `recovery-code.ts` | `src/utils/recovery-code.ts` | ✅ **已审计** |
| `response.ts` | `src/utils/response.ts` | ✅ **已审计** |
| `totp.ts` | `src/utils/totp.ts` | ✅ **已审计** |
| `user-decryption.ts` | `src/utils/user-decryption.ts` | ✅ **已审计** |
| `uuid.ts` | `src/utils/uuid.ts` | ✅ **已审计** |
| `api.ts` | `webapp/src/lib/api.ts` | ✅ **已审计** |
| `crypto.ts` | `webapp/src/lib/crypto.ts` | ✅ **已审计** |
| `export-formats.ts` | `webapp/src/lib/export-formats.ts` | ✅ **已审计** |
| `i18n.ts` | `webapp/src/lib/i18n.ts` | ✅ **已审计** |
| `import-formats.ts` | `webapp/src/lib/import-formats.ts` | ✅ **已审计** |
| `password-breach.ts` | `webapp/src/lib/password-breach.ts` | ✅ **已审计** |
| `ssh.ts` | `webapp/src/lib/ssh.ts` | ✅ **已审计** |
| `types.ts` | `webapp/src/lib/types.ts` | ✅ **已审计** |
| `vite-env.d.ts` | `webapp/src/vite-env.d.ts` | ✅ **已审计** |
| `vite.config.ts` | `webapp/vite.config.ts` | ✅ **已审计** |

</details>

--- 

## ⚠️ 操作指南

如果您看到 **FAIL** 状态或严重的代码问题：
1. **开发人员**：使用上方表格中的 **位置** 列找到确切的文件和行号。
2. **纠正**：遵循为每个规则提供的文档链接以提交修复。
3. **可追溯性**：完整的原始 `.sarif` 数据已附加到此分支。下载并将其导入您的 IDE（例如 VS Code SARIF 查看器）进行本地分析。

--- 

💡 *由 Antigravity AI 安全引擎生成。透明度是我们的承诺。*