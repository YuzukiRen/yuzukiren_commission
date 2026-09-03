# Blivechat 蓝色蝴蝶结弹幕样式

以 `弹幕 拷贝.png` 为视觉参考，使用原文件夹内的普通用户、房管、舰长、SC 与航海提醒素材制作。

## 安装（本地版 Blivechat）

1. 把整个 `blivechat-theme` 文件夹复制到 Blivechat 的 `data/custom_public/` 中。
2. 将本目录 `preset.css` 的一行内容复制到以下任一位置：
   - Blivechat 的 `data/custom_public/preset.css`，然后在设置中启用“导入服务器预设 CSS”；
   - OBS 浏览器源的“自定义 CSS”。
3. OBS 浏览器源推荐宽度 `640px`；这是原素材的 1:1 像素构图宽度。高度按版面需要设置，通常 `800–1200px`。

最终导入语句为：

```css
@import url("/custom_public/blivechat-theme/theme.css");
```

> 在线公共版 `blive.chat` 无法直接读取你电脑上的素材。若使用公共版，需要先把整个文件夹上传到可公开访问的静态网站，再将上面的导入地址替换为 `theme.css` 的完整 HTTPS 地址。

## 文件

- `theme.css`：正式样式。
- `native-scale.css`：按 PSD 导出层原始像素定位的 1:1 构图覆盖层，由 `theme.css` 自动导入。
- `preset.css`：可粘贴到 Blivechat/OBS 的导入语句。
- `preview.html`：本地预览，包含参考短弹幕与三类长弹幕换行测试。
- `assets/`：框体、装饰、头像框与小赖字体。

预览页不会生成或附带头像占位图，只展示素材中原有的透明头像框；接入 Blivechat 后，真实用户头像会落在对应开孔内。

## 自定义

在 `theme.css` 顶部 `:root` 中可以修改主要颜色、字体以及是否显示 SC 固定栏。默认隐藏固定栏，对应：

```css
--blue-chat-ticker-display: none;
```

需要显示时改为 `block`。

此主题针对当前 Blivechat 的 YouTube 风格 DOM，覆盖普通弹幕、舰队成员、房管、主播、上舰提示、礼物与醒目留言；已隐藏时间、原生勋章、输入栏和滚动条。
