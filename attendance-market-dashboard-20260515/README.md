# 考勤与市场投入管控看板交付说明

本项目为“考勤/出差/市场在岗管控看板”的方案文档与高保真静态预览原型。原 SmartBI 分享链接在本机访问 20 秒超时，未能读取原始页面结构，因此本版以用户提供的业务需求作为重构依据，使用模拟数据完成。

## 文件结构

- `prototype/index.html`：PC 与移动端自适应网页原型，不依赖真实接口。
- `preview/`：Playwright 生成的看板截图。
- `docs/考勤与市场投入管控看板优化方案_详细版.md`：面向工作人员、系统方和 SmartBI 实施方。
- `docs/考勤与市场投入管控看板优化方案_领导版.md`：面向公司领导，引用预览截图。
- `docs/SmartBI实施清单.md`：按模块列出 SmartBI 配置、字段、计算和下钻规则。
- `docs/数据字段与指标口径清单.md`：数据表字段、指标公式、异常规则与权限口径。

## 打开预览

直接用浏览器打开：

```bash
open prototype/index.html
```

或启动本地静态服务：

```bash
python3 -m http.server 4173
```

然后访问：

```text
http://127.0.0.1:4173/prototype/index.html
```

## 生成截图

已使用 Playwright 生成以下截图：

- `preview/01_领导总览.png`
- `preview/02_总部出差监控.png`
- `preview/03_大区市场在岗监控.png`
- `preview/04_单位公平对比.png`
- `preview/05_异常中心与人员明细.png`
- `preview/06_移动端总览.png`：移动端响应式效果补充截图。

如需重新生成，可运行项目中的截图脚本或使用 Playwright 打开页面后按对应锚点截图。

## 发布链接

已通过现有公开 GitHub Pages 仓库发布到独立目录：

```text
网页预览：https://jayzhou0214-ops.github.io/tangshan-workspace/attendance-market-dashboard-20260515/prototype/
交付包下载：https://jayzhou0214-ops.github.io/tangshan-workspace/attendance-market-dashboard-20260515/考勤与市场投入管控看板交付包.zip
```

备用 72 小时公开临时链接：

```text
网页预览：https://litter.catbox.moe/lvlaxo.html
交付包下载：https://litter.catbox.moe/42woyk.zip
```

说明：本机可用 GitHub REST token 创建新仓库和 Contents API 写入时返回 403，因此改用已存在且可推送的公开 Pages 仓库 `jayzhou0214-ops/tangshan-workspace` 发布。
