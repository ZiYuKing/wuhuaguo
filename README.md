# 无花果短剧 

<p align="center">
  面向 iOS、Android 手机与 Android TV 的跨平台短剧播放客户端
</p>

<p align="center">
  原生播放器 · 上下滑切集 · 离线下载缓存 · 手机投屏 TV · 三端授权
</p>

## 项目简介

无花果短剧是一款针对短剧观看场景设计的跨平台客户端，覆盖 iOS、Android 手机和 Android TV。在 Android 与 iOS 上分别接入原生播放器，以兼顾多端一致性、硬件解码能力和高频切集时的流畅体验。

项目提供`首页推荐`、`分类浏览`、`全局搜索`、`热播榜单`、`分享内容识别`、`上下滑切集`、`弹幕`、`收藏`、`历史记录`、`离线下载`、`局域网投屏`等功能。安卓 TV 端拥有独立的大屏布局和遥控器焦点系统，并可作为手机端的投屏接收端。

无花果短剧不提供、存储或分发任何影视内容。项目仅用于播放器技术研究、跨端应用实践和合法授权内容的个人使用。使用者应自行确保数据来源、接口权限及内容使用行为符合所在地法律法规和相关平台规则。

## 体验与下载

| 平台 | 当前形态 | 获取方式 | 主要架构 |
|---|---|---|---|
| iOS | 手机客户端 | 请前往 [Releases](https://github.com/ZiYuKing/wuhuaguo/releases) | Apple 真机 |
| Android 手机 | 手机客户端 | 请前往 [Releases](https://github.com/ZiYuKing/wuhuaguo/releases) | `arm64-v8a` |
| Android TV | 独立大屏客户端 | 请前往 [Releases](https://github.com/ZiYuKing/wuhuaguo/releases) | `armeabi-v7a` 32 位 |

> 安装后需要有效授权才能进入应用。授权可按平台分别开通，也可以同时包含 iOS、Android 手机和 Android TV。

## 界面预览

### 手机端首页
<img width="421" height="936" alt="image" src="https://github.com/user-attachments/assets/4a683824-49fe-4ee2-b2bc-8aea48b3d8e2" />
<img width="421" height="936" alt="image" src="https://github.com/user-attachments/assets/fbcb2d03-10aa-455c-9a60-9403b26b8a44" />
<img width="421" height="936" alt="image" src="https://github.com/user-attachments/assets/11ed2be9-7cc0-4663-aa01-cf8d228ce2fd" />

首页围绕快速发现内容设计，支持轮播推荐、继续观看、分类内容流和热播榜单入口。顶部提供搜索与扫码入口，底部使用模糊透明的 Liquid Glass 导航。

### 搜索、榜单与详情
<img width="421" height="936" alt="image" src="https://github.com/user-attachments/assets/d78eb760-734b-4021-8a71-ebfec831b10c" />
<img width="421" height="936" alt="image" src="https://github.com/user-attachments/assets/bb59e285-1a95-4556-ba6b-7c64f6f948b1" />
<img width="421" height="936" alt="image" src="https://github.com/user-attachments/assets/3e9c2186-9697-448e-8637-c1d00416a180" />
<img width="421" height="936" alt="image" src="https://github.com/user-attachments/assets/66f3daa0-55c7-4d88-addf-4db730d15f9c" />

支持按短剧名称、演员、作者或题材搜索；榜单提供多个内容分类和分页浏览；详情页集中展示海报、简介、标签、集数、收藏状态、续播位置与下载入口。

### 播放器
<img width="1600" height="940" alt="image" src="https://github.com/user-attachments/assets/1cfed3d8-7067-461b-9c85-959f7952b9bd" />
<img width="421" height="936" alt="image" src="https://github.com/user-attachments/assets/17fb1b5c-bf3d-4a19-a670-a9d8d3cef556" />
<img width="935" height="421" alt="image" src="https://github.com/user-attachments/assets/6030ca83-785f-4f75-8d59-e3e0964311bb" />
<img width="935" height="421" alt="image" src="https://github.com/user-attachments/assets/7f3a6726-0434-4fcb-b820-0637712f27a8" />
<img width="420" height="882" alt="image" src="https://github.com/user-attachments/assets/a63ea5f4-abe1-4b64-9392-9f41bc22220a" />

播放器针对连续短剧观看进行了专门优化，支持上下滑切集、横竖屏切换、选集、清晰度、倍速、弹幕、收藏、下载、投屏和定时关闭。控制层会根据屏幕方向重排，减少对画面的遮挡。

### Android TV
<img width="1600" height="898" alt="image" src="https://github.com/user-attachments/assets/73d6ef9a-2030-4f14-921d-f085ebed0866" />
<img width="1600" height="895" alt="image" src="https://github.com/user-attachments/assets/d2a00d88-57c4-4318-98dc-b09e998701ee" />
<img width="1600" height="895" alt="image" src="https://github.com/user-attachments/assets/f1fe4979-f399-4d0f-ac36-78f27cc9e4ad" />

TV 端采用独立横屏界面，提供首页、搜索、榜单、我的和设置五个主要区域。所有操作均针对遥控器方向键、确认键和返回键设计，包含清晰的焦点反馈、默认焦点、跨区域导航和自动滚动定位。


## 核心功能

### 内容发现

- 首页轮播与分类推荐。
- 真人剧、漫剧、AI 剧等内容分类。
- 继续观看与续播集数提示。
- 多分类热播榜单与分页加载。
- 全局搜索、搜索联想和搜索历史管理。
- 详情页海报、简介、标签、集数和相关元信息展示。
- 分享链接与整段分享文案识别。
- 可信分享内容自动识别，并在用户确认后进入播放。


### 收藏、历史与下载

- 本地观看记录与最后播放进度。
- 收藏短剧并在手机或 TV 的“我的”页面快速访问。
- 按集多选下载、全选、暂停、继续和失败重试。
- 全局下载队列与并发控制。
- 后台下载状态同步与下载通知。
- 下载文件完整性检查，避免把空文件或损坏文件误报为完成。
- 已下载内容离线播放。
- 按单集或整部短剧删除本地文件。
- 损坏记录隔离和可恢复数据保留。

### 手机投屏到 TV

- 自动发现同一局域网内的无花果短剧 TV。
- 手机端选择电视后发送当前短剧、集数和播放进度。
- TV 端显示配对确认并接收播放任务。
- 限制在局域网内通信，拒绝非本地网络请求。
- 手机与 TV 使用版本化投屏协议，避免不兼容指令误播放。

## 三端设计

| 能力 | iOS | Android 手机 | Android TV |
|---|:---:|:---:|:---:|
| 首页推荐与分类 | ✅ | ✅ | ✅ |
| 搜索与榜单 | ✅ | ✅ | ✅ |
| 详情、选集与续播 | ✅ | ✅ | ✅ |
| 原生播放器 | AVPlayer | Media3 ExoPlayer | Media3 ExoPlayer |
| 上下滑切集 | ✅ | ✅ | 遥控器切集 |
| 横屏播放 | ✅ | ✅ | 默认横屏 |
| 弹幕 | ✅ | ✅ | ✅ |
| 收藏与观看记录 | ✅ | ✅ | ✅ |
| 离线下载 | ✅ | ✅ | — |
| 发起投屏 | ✅ | ✅ | — |
| 接收手机投屏 | — | — | ✅ |
| 激活码授权 | ✅ | ✅ | ✅ |
| 扫码激活其他设备 | ✅ | ✅ | — |
| 展示二维码等待激活 | ✅ | ✅ | ✅ |
| 遥控器焦点导航 | — | — | ✅ |

## 数据与隐私

- 观看记录、收藏、下载记录和客户端设置默认保存在本机。
- 激活凭证使用系统安全存储，不以明文写入普通偏好设置。
- 扫码激活使用短时有效的一次性配对信息，不在二维码中包含真实激活码。
- 局域网投屏仅用于发现和连接同一网络中的 TV 端。
- 卸载应用后，本机保存的数据可能被系统一并清除。
- 项目不提供用户账号体系，也不主动托管用户的观看记录。


## 免责声明

本项目仅用于学习、研究和合法授权场景下的技术交流，不提供任何影视内容、内容索引服务或商业内容授权。项目名称、界面截图及功能描述不代表与任何第三方平台存在官方关系。

使用者应遵守适用的法律法规、服务协议、著作权规则和网络访问政策。因使用者自行配置的数据来源、接口或内容所产生的任何责任，由使用者自行承担。
