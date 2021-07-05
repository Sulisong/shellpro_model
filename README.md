# shellpro_model

**带壳截图Pro_第三方模块共享库**

---
路径详情
* /model/ 模块数据路径
* /model/brands.json 机型分类（如果上传没有分类，可以创建）示例：

```
"小米": {
    "bg_color": "0xFFFF6700",// 卡片背景
    "png": "ic_xiaomi.png",// 标头图片名称，图片位置：/png
    "home": "xiaomi",// 模块仓库（仓库路径使用英文小写），例如：/model/xiaomi/
    "have_3d": true,// 是否包含3D模块
    "have_more": false// 是否包含多模板模块
}
```

* /model/***/dl.json 模块列表（上传模块后在列表添加）示例：

```
"小米 Alpha": {
    "author": "xxxx",//作者名称
    "mode": "3d"//模块模式[2d、3d、more]，分别位图片模块、3D模块、多模板模块
}
```

* /model/***/zip/ 存放模块zip压缩包路径，格式为dl.json‘添加的名称.zip’
* /model/***/preview/ 模块预览图，推荐分辨率大小120，名称格式为dl.json‘添加的名称.jpg’
* /png/ 标头图片等目录
---
**上传模块流程**
推荐使用VSCode 克隆项目，本地操作上传（或者直接网页克隆项目，完成以下步骤请求拉取即可）
* 软件内使用‘导入模块’功能导入模块
* 在导入模块列表选择模块左滑，点击分享按钮生成‘zip’至手机/sdcard/ShellPro路径
* 在/model/brands.json 添加机型分类，已存在则跳过
* 在模块仓库dl.json 添加模块参数
* 在模块仓库/zip/上传模块zip
* 在模块仓库/preview/上传预览图jpg
* 最后提交拉取请求等待仓库管理员合并仓库
