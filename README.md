### GitHub图片路径替换工具

**项目简介**

这是一个专门用于处理GitHub下载的Markdown文档中图片链接的Python脚本工具。它能够智能识别并替换GitHub仓库中的图片链接为本地相对路径，同时保留其他外部图片链接不变，有效解决从GitHub克隆文档后图片无法显示的问题。功能特点

### 🎯 精准替换

* **只替换GitHub图片链接**：仅针对`https://github.com/`开头的图片链接进行替换
  
* **保留外部图片**：自动保留其他外部图片链接（如`https://image.3001.net/`等）
  
* **智能识别**：使用正则表达式精确匹配GitHub仓库图片路径格式
  

### 📁 双重处理模式

* **单文件处理**：针对单个Markdown文件进行图片链接替换
  
* **批量处理**：递归处理整个文件夹中的所有Markdown文件
  

### 🔧 灵活配置

* **路径模板**：使用`{filename}`占位符，灵活配置新图片路径
  
* **试运行模式**：预览替换效果，避免误操作
  
* **详细日志**：显示处理进度和替换详情
  

### 📊 完整报告

* 显示找到的GitHub图片链接数量
  
* 展示每个链接的替换详情
  
* 统计保留的外部图片链接
  
* 批量处理时提供总体统计信息
  

安装要求

* Python 3.6+
  
* 无需额外依赖库
  

使用方法

### 基本使用

1. 下载脚本文件
  
2. 运行脚本：bashpython github_image_replacer.py
  

### 交互式操作步骤

1. **选择处理模式**text请选择处理模式:1. 处理单个文件2. 批量处理文件夹
  
2. **配置新图片路径**
  
  * 使用`{filename}`作为图片文件名的占位符
    
  * 示例：`./images/{filename}` 或 `D:/文档/项目/images/{filename}`
    
3. **选择运行模式**
  
  * 试运行模式(`y`)：只预览替换效果，不修改文件
    
  * 实际运行模式(`n`)：实际执行替换操作
    

### 使用示例

#### 示例1：处理单个文件


请输入Markdown文件路径: .\域渗透-Delegation.md请输入新的图片路径模式: D:/红队/技术文档/Active-Directory-Pentest-Notes-master/images/{filename}是否试运行? (y/N): n
<img width="1698" height="506" alt="image" src="https://github.com/user-attachments/assets/201a3ab9-b7ca-4395-84c3-6d0b799370f7" />


#### 示例2：批量处理文件夹


请输入文件夹路径: D:/技术文档/Markdown文档请输入新的图片路径模式: ./assets/images/{filename}是否试运行? (y/N): y替换效果
<img width="1716" height="813" alt="image" src="https://github.com/user-attachments/assets/2b09fd83-35e7-4288-bc34-9c9bb98a85ad" />


### 替换前


<img width="2123" height="1279" alt="image" src="https://github.com/user-attachments/assets/3fd57354-4aa4-4528-8702-f0f7269269c7" />


### 替换后

<img width="2141" height="1343" alt="image" src="https://github.com/user-attachments/assets/64effb56-0bbc-4214-933f-b726b053fc07" />


### 🚀 GitHub文档本地化

从GitHub克隆技术文档、笔记或电子书后，快速将图片链接转换为本地路径，确保文档完整性。

### 📚 知识库迁移

将基于GitHub的文档迁移到本地或其他平台时，批量处理图片引用。

### 🔄 文档备份

为GitHub上的Markdown文档创建完整可用的本地备份版本。技术细节

### 支持的图片格式

* PNG (`*.png`)
  
* JPG/JPEG (`*.jpg`, `*.jpeg`)
  
* GIF (`*.gif`)
  
* BMP (`*.bmp`)
  
* SVG (`*.svg`)
  
* WebP (`*.webp`)
  

### 匹配规则

脚本使用正则表达式精确匹配GitHub图片路径格式：

https://github.com/用户名/仓库名/blob/(master|main)/images/文件名.扩展名

### 文件编码

* 读取/写入均使用UTF-8编码
  
* 支持包含中文等特殊字符的文件路径
  

注意事项

1. **备份重要文件**：建议在处理前备份重要文档，或先使用试运行模式预览效果
  
2. **路径一致性**：确保新的图片路径模式与实际图片存放位置一致
  
3. **权限检查**：确保脚本有权限读取和修改目标文件
  
4. **编码兼容**：如遇编码错误，请检查文件是否为UTF-8格式
  

### 常见问题

**Q: 脚本提示"未找到GitHub图片路径"**A: 检查文档中的图片链接是否符合GitHub标准格式，或确认链接是否已为本地路径

**Q: 替换后图片仍无法显示**A: 检查新路径是否正确，确认图片文件实际存在于指定位置

**Q: 处理含特殊字符的文件时出错** A: 确保文件路径不包含脚本无法处理的特殊字符更新日志

### v1.0.0

* 初始版本发布
  
* 支持单文件和批量处理模式
  
* 添加试运行功能
  
* 完整的替换报告
  

贡献

欢迎提交Issue和Pull Request来改进这个工具！

* * *

**使用这个工具，让GitHub文档的本地化管理变得简单高效！** 🎉# markdown_img_script
