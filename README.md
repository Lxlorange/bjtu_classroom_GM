# BJTU 教室空闲查询助手油猴版

![Version](https://img.shields.io/badge/version-3.3-blue) ![Tampermonkey](https://img.shields.io/badge/Platform-Tampermonkey-green)

一个用于北京交通大学教学服务平台 (aa.bjtu.edu.cn) 的油猴脚本。它能在你浏览教室查询页面时，自动抓取所有分页数据，并智能筛选出当前可用的自习教室。

## 主要功能

* **全量扫描**：自动在该教学楼的所有分页（Page 1~N）中查找空闲教室，点击进入页面会直接显示所有的结果，也可以用原本教务系统的筛选功能搜索，脚本会按照搜索结果聚合整理出空闲教室。
* **智能筛选**：
    * **全天空闲**：自动计算上午(1-2)、下午(4-5)、晚上(7)的全交集。
    * **分时段展示**：分别列出上午、下午、晚上的空闲教室。
* **双语支持**：兼容教务系统的中文界面与英文界面。
* **视觉增强**：
    * 按楼宇优先级排序（逸夫 > 思源 > 思源西 > 思源东），可以按个人习惯在代码中自行修改。
    * 不同教学楼使用不同颜色高亮（🟩 逸夫 / 🟦 思源 / 🟥 西楼 / 🟧 东楼）。
* **无需配置**：安装即用，基于当前页面的 Cookie 自动鉴权，无需额外登录。

## 安装方法

1.  安装浏览器扩展 [Tampermonkey](https://www.tampermonkey.net/) (Chrome/Edge/Firefox)。
2.  前往 [Greasy Fork](https://greasyfork.org/zh-CN) (推荐) 或 GitHub Release 下载脚本。
3.  点击“安装”即可。

## 使用说明

1.  登录 [BJTU 教学服务平台](https://aa.bjtu.edu.cn/classroomtimeholdresult/room_view/)。
2.  进入“教室占用查询”页面，选择**周次**和**教学楼**，或什么也不选。
3.  脚本会自动运行，在页面右侧生成一个黑色半透明浮窗。
4.  进度条跑满后，即可查看整理好的空闲教室列表。

## 致谢

受吴老师的版本的启发所作。考虑到部分同学可能不方便配置本地 Python 环境，我将其逻辑移植到了浏览器前端，利用油猴脚本实现了轻量化的“即开即用”体验。

* **原 Python 项目仓库**：[https://github.com/mustbeasaltyfish/bjtu_classroom_query.git]

## 开源协议

MIT License