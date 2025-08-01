# 自选基金助手

自选基金助手，实时查看您关注的基金，助您快速获取实时数据。

可以用来查看您的自选基金的实时估值情况，可以自由的增减自选基金。您的自选基金数据会跟随账号同步。

## 介绍

买了基金后，一直想找一款 pc 端的 chrome 扩展插件，毕竟股票的交易时间都是在工作日进行的，可惜找不到，便打算自己写一个，忍痛花费 5 美刀上架扩展商店。扩展的形式很适合上班族，不用打开网站，仅以小窗口的形式展示，不会引起 BOSS 的注意，方便上班摸鱼。

首先输入基金代码添加基金，涨跌幅信息和收益信息可以以角标的形式展示在浏览器中，更加简便直观。可以在设置中单独开启显示份额与收益选项，在编辑中输入持有的份额，可以计算出每个基金的实时估值与收益，以及总收益。

## 主要功能

- 实时角标提醒
- 单个基金特别关注
- 角标内容自定义，单个与全部基金，收益额与收益率
- 支持标准与暗色两种主题
- 基金列表与配置信息支持导入与导出
- 智能判断节假日，切换休市状态
- 支持设置份额或金额，查看当日估值收益
- 支持设置持仓成本价，查看持有收益
- 支持手动加仓减仓功能
- 支持账号登录功能，方便跨平台同步
- 交易日更新当日实际净值后，对应基金有 √ 提示
- 支持查看估值走势图，净值、收益等走势图
- 支持支持查看基金的股票持仓明细
- 支持查看基金基本信息与基金经理信息
- 自定义顶部指数内容
- 自定义基金列表展示内容
- 指数与基金拖拽排序功能
- 基金按照指定项排序功能
- 添加基金时支持按拼音、汉字、编码模糊搜索，支持批量添加
- 行情中心展示，两市资金、行业板块、北向资金、南向资金

## 如何使用

**强烈推荐使用 Chrome 商店安装**（这样才能获得自动更新）：[点击跳转至 Chrome 扩展商店](https://chrome.google.com/webstore/detail/dhdelcemeednchdmijiocipbjlknndff)

若因网络问题，可以下载 CRX 文件手动安装（无法自动更新最新版）：[下载地址 1](https://github.com/x2rr/funds/releases)　[下载地址 2](https://gitee.com/rabt/funds/releases)

插件已上架 Microsoft Edge 扩展商店：[点击跳转至 Microsoft Edge 扩展商店](https://microsoftedge.microsoft.com/addons/detail/kophadiajpobbfoobhclbobddkoindoi)

插件已上架火狐 Firefox 扩展商店：[点击跳转至火狐 Firefox 扩展商店](https://addons.mozilla.org/zh-CN/firefox/addon/funds/)

插件推出小程序版‘韭菜计算助手’欢迎使用！

![小程序](https://gitee.com/rabt/Picture/raw/master/img/mp.jpg)

![主界面1](https://gitee.com/rabt/Picture/raw/master/img/20200717165330.png)

![主界面2](https://gitee.com/rabt/Picture/raw/master/img/20200916120011.png)

![主界面3](https://gitee.com/rabt/Picture/raw/master/img/20200916120012.png)

![主界面4](https://gitee.com/rabt/Picture/raw/master/img/20200907111218.png)

![主界面5](https://gitee.com/rabt/Picture/raw/master/img/20200907111226.png)

## 框架介绍

基于[Vue](https://github.com/vuejs/vue) + [Webpack](https://github.com/webpack/webpack)构建的 vue 项目，使用了[vue-web-extension](https://github.com/Kocal/vue-web-extension/tree/v1)模板快速构建Chrome扩展项目，用到了[Element UI](https://github.com/ElemeFE/element)样式库与[ECharts](https://github.com/apache/echarts)图表库。

## 运行调试开发

需要 node 环境，先执行
`npm i`
安装依赖

调试模式执行
`npm run watch:dev`
生成 dist 文件夹，浏览器选择“加载已解压的扩展程序”

打包与发布先执行
`npm run build`
生成 dist 文件夹，再执行
`npm run build-zip`
通过从 manifest.json 文件中读取 name 和 version 字段,构建{name}-v{version}.zip 这种格式的压缩文件。

## 更新说明

### v3.0.3

- 优化加仓功能的计算方式。

### v3.0.2

- 修复角标与弹窗内容不一致的问题。
- 修复加仓后成本小数点异常的问题。

### v3.0.0

- 支持账号登录功能，方便跨平台同步（对应的增加了阿里云 bspapp.com 访问权限）。
- 支持手动加仓减仓功能。
- 编辑基金信息时支持份额金额二选一输入。
- 修复基金累计收益曲线异常问题、基金持有收益率计算问题。
- 其他问题修复与优化。

### v2.5.1

- 修复基金信息的 Excel 导入导出功能。

### v2.5.0

- 支持基金信息的 Excel 导入导出功能。
- 支持锁定并保持基金的排序方式。
- 行情中心支持查看当日交易额与涨跌数量信息。
- 问题修复与优化。

### v2.4.2

- 支持以文本的方式导入导出配置信息。
- 行情中心支持查看北向资金、南向资金信息。
- 问题修复与优化。

### v2.4.1

- 修复新版本出现的问题。

### v2.4.0

- 增加行情中心，支持查看大盘资金流向、行业版块资金流向。
- 基金详情页添加基金概况信息，支持查看基金经理详情。
- 编辑页面支持调节页面灰度与透明度。
- 页面布局调整，修复历史遗留问题。

### v2.3.1

- 修复一个影响性能的定时任务问题。

### v2.3.0

- 新增独立窗口模式，右击插件图标，选择进入即可。
- 添加手动刷新按钮。
- 修复大盘与股票走势图中，鼠标移出时卡死的问题。

### v2.2.1

- 解决火狐浏览器手机版更新日志无法点击的问题。

### v2.2.0

- 大盘指数支持查看走势图。
- 持仓明细中可点击对应股票直接查看走势图。
- 页面布局调整，金额小数点位数调整。

### v2.1.1

- 持仓明细中可点击对应股票跳转至网站详情。
- 合并单位净值与累计净值，详情中增加日增长率。
- 页面布局调整。

### v2.1.0

- 支持查看基金的持仓明细。
- 角标内容支持选择指数。
- 走势图支持更多区间选择。
- 页面字号新增两档可调节，其他页面布局调整。

### v2.0.9

- 修复角标金额上 k 时颜色异常问题。
- 修复导入配置后角标未更新的问题。

### v2.0.8

- 调整节假日信息链接。

### v2.0.7

- 优化代码，修改插件主页。

### v2.0.6

- 修复单个基金角标颜色异常的问题。

### v2.0.5

- 修复个别基金估值收益异常问题。
- 界面布局对齐方式调整。

### v2.0.4

- 修复角标 NAN 问题。
- 修复更新日志无法关闭问题。

### v2.0.3

- 修复一系列 bug,优化代码。
- 添加交流群，欢迎交流与反馈。

### v2.0.2

- 修复个别基金数据异常的 bug。

### v2.0.0

- 调整基金接口，支持当日实际净值，已更新的基金会有 √ 提示。
- 角标支持自定义功能，单个、全部、收益率、收益额，随心所欲。
- 支持查看历史更新日志功能。

### v1.8.0

- 新增查看基金详情功能，点击基金名称即可查看估值图、走势图等相关信息。
- 新增基金配置信息的导入导出功能。
- 修复页面布局中的 bug。

### v1.7.1

- 新增查看持有收益功能，添加持仓成本后，可以统计持仓总收益。
- 修复设置页面中的 bug。

### v1.7.0

- 新增暗色模式主题。
- 顶部指数信息支持动态修改。
- 暂停实时更新功能改为全局生效。
- 修复删除特别关注的基金后，脚本还实时更新的异常。

### v1.6.0

- 解决基金添加后无法显示、基金丢失等异常问题。
- 增加按类别排序功能。
- 增加拖拽排序功能。
- 添加基金时增加搜索与多选功能。

### v1.5.6

- 修复不同时区的时间异常问题。

### v1.5.5

- 改个名字，φ(>ω<\*) 听说名字越长越厉害。
- 优化滚动条效果，调整页面布局。
- 优化基金名称过长时的显示效果。

### v1.5.4

- 有小伙伴反馈找不到设置入口，现在主页面增加设置入口，主页面布局调整。
- 设置页增加源码入口，感兴趣的小伙伴可以帮忙点个 star。

### v1.5.3

- 优化持有金额与估值收益的计算方式，持有金额为上一个结算日的金额，估值收益为当前估算的收益额。
- 添加基金总收益项。

### v1.5.2

- 优化页面布局，拆分份额与收益信息选项。

### v1.5.1

- 功能优化。

### v1.5.0

- 增加基金排序功能。
- 新增设置选项，右键应用选择‘选项’即可进入设置。
- 完善节假日信息，可在设置中更新最新节假日信息。
- 增加收益估算功能，填写持有份额后即可自动计算每日收益，需在设置中开启。

### v1.4.3

- 解决因个别新发行基金数据错误而产生的数据异常问题。

### v1.4.2

- 修复休市中角标颜色异常的 bug。

### v1.4.1

- 涨跌颜色调整。

### v1.4.0

- 优化代码，完善功能。

### v1.3.2

- 优化特别关注功能。

### v1.3.1

- 增加特别关注功能，实时角标提醒；
- 增加简单的休市逻辑，休市状态不再实时更新数据。

### v1.2.0

- 修复个别基金数据无法正常获取的问题；

## 隐私协议

[点击跳转](https://x2rr.github.io/funds/privacy.html)  

