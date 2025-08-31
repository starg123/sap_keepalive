# SAP CF 自动保活脚本

本脚本用于在 SAP BTP Cloud Foundry 中自动保活应用，每天按 UTC 时间在 **0:15、0:35、0:55** 自动执行保活操作。

---

## 需要的 Secrets

| Secret 名称      | 说明 |
|-----------------|--------------------------------------------------|
| `CF_USERNAME`    | 你的 SAP BTP Cloud Foundry 登录用户名（通常是邮箱） |
| `CF_PASSWORD`    | 你的 Cloud Foundry 登录密码 |
| `CF_API`         | Cloud Foundry API endpoint，例如：`https://api.cf.ap21.hana.ondemand.com` |
| `CF_ORG`         | 你的组织名 (Org) |
| `CF_SPACE`       | 你的空间名 (Space) |
| `CF_APP`         | 你要保活的应用名称 (App name) |

---

## 配置方法

1. 打开 GitHub 仓库 → **Settings** → **Secrets and variables** → **Actions**。
2. 点击 **New repository secret**，依次添加上面列出的 Secrets。
3. **注意**：名称必须和 workflow 文件里一致（例如 `CF_USERNAME`）。
4. 值就是你在 SAP BTP Cloud Foundry 上对应的参数。

---

## 查询参数命令

```bash
cf t
cf a

