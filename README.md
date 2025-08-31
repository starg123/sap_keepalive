SAP CF 自动包活脚本：
UTC 时间，每天 0:15、0:35、0:55 自动执行保活操作。

需要的 Secrets
Secret名称	说明
CF_USERNAME	你的 SAP BTP Cloud Foundry 登录用户名（通常是邮箱）。
CF_PASSWORD	你的 Cloud Foundry 登录密码。
CF_API	Cloud Foundry API endpoint，例如：https://api.cf.ap21.hana.ondemand.com。
CF_ORG	你的组织名 (Org)。
CF_SPACE	你的空间名 (Space)。
CF_APP	你要保活的应用名称 (App name)。

配置方法

打开 GitHub 仓库 → Settings → Secrets and variables → Actions。

点击 New repository secret，依次添加上面几个变量。

名称必须和 workflow 里写的一样（例如 CF_USERNAME）。

值就是你在 SAP BTP Cloud Foundry 上对应的参数。

查询参数命令：
cf t
cf a
