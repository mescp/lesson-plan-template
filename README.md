# 教案模板编辑器

这是一个基于Web的模板编辑器应用程序，专门用于编辑教案模板。该应用允许用户上传底图和对应的JSON模板，在保持元素位置不变的情况下修改文本内容，并导出修改后的JSON文件。

## 功能特点

### 1. 文件处理
- 支持上传底图（JPG/PNG格式）
- 支持上传JSON模板文件
- 支持导出修改后的JSON文件
- 自动保存编辑状态到浏览器本地存储

### 2. 编辑功能
- 左侧面板显示所有可编辑的文本项
- 文本框自动调整高度以适应内容
- 编辑时自动定位到对应的预览区域
- 实时预览编辑效果

### 3. 预览功能
- 右侧实时预览底图和文本叠加效果
- 自动计算缩放比例，确保文本位置准确
- 支持滚动查看大图
- 编辑时高亮显示当前编辑的文本区域

### 4. 复制功能
- 支持复制任意文本区域的内容
- 提供复制按钮和点击复制两种方式
- 复制成功时显示提示信息

### 5. 本地存储
- 自动保存编辑状态
- 页面刷新后自动恢复上次的编辑状态
- 包括底图、JSON数据和文件名的存储

## 技术实现

### 单位转换
- JSON模板中的宽度和高度单位为厘米(cm)
- 自动转换为像素显示（1cm = 37.8px，基于96dpi）
- 自动计算缩放比例，确保显示准确

### 布局设计
- 使用Flex布局实现左右分栏
- 左侧为编辑面板，右侧为预览区域
- 响应式设计，适应不同屏幕尺寸

### 文本处理
- 使用绝对定位确保文本准确覆盖在底图上
- 保持原始JSON中的位置信息不变
- 只允许修改文本内容

## 使用指南

### 1. 开始使用
1. 在浏览器中打开`index.html`文件
2. 界面分为左右两个面板：
   - 左侧：控制面板，包含文件上传和文本编辑
   - 右侧：预览区域，显示底图和文本效果

### 2. 上传文件
1. 点击"上传底图"按钮选择图片文件（支持JPG/PNG）
2. 点击"上传JSON模板"按钮选择JSON文件
3. 文件上传后会自动显示预览效果

### 3. 编辑文本
1. 在左侧面板中找到需要编辑的文本框
2. 直接在文本框中修改内容
3. 修改会实时显示在右侧预览区域
4. 编辑时，右侧对应的文本区域会自动高亮并滚动到可视区域

### 4. 复制文本
1. 将鼠标悬停在右侧预览区域的任意文本上
2. 点击出现的"复制"按钮或直接点击文本区域
3. 文本会被复制到剪贴板
4. 右上角会显示"复制成功！"提示

### 5. 保存功能
1. **自动保存**：
   - 编辑过程中会自动保存到浏览器本地存储
   - 刷新页面后会自动恢复上次的编辑状态

2. **手动保存**：
   - 点击"保存到缓存"按钮手动保存当前状态
   - 保存成功会显示提示信息

3. **导出JSON**：
   - 点击"导出JSON"按钮
   - 输入要保存的文件名（默认使用上传的文件名）
   - 确认后会下载修改后的JSON文件

## 注意事项

1. 本应用完全在浏览器端运行，无需服务器
2. 建议使用现代浏览器（Chrome、Firefox、Edge等）
3. 本地存储空间有限，请注意图片大小
4. 编辑只影响文本内容，不会改变位置和样式信息

## 技术栈

- HTML5
- CSS3
- JavaScript (ES6+)
- 本地存储 (LocalStorage)
- FileReader API
- Clipboard API

## 浏览器支持

- Chrome (推荐)
- Firefox
- Edge
- Safari

## 未来改进方向

1. 添加字体选择功能
2. 支持批量处理多个模板
3. 添加更多预设模板
4. 优化大文件处理性能
5. 添加撤销/重做功能
6. 支持更多图片格式 