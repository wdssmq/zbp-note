# 从剪贴板粘贴图片

安装 [vscode-paste-image](https://github.com/mushanshitiancai/vscode-paste-image) 扩展后，可以使用 `cmd+alt+v` 从剪贴板粘贴图片。

图片会自动复制到 `/attachments` 文件夹，并在粘贴图片的文件中添加引用。

系统会提示你确认图片名称。要禁用此提示，请在设置中添加 `"pasteImage.showFilePathConfirmInputBox": false,`。

要更改图片的创建位置，请修改 `pasteImage.path` 属性，例如：

- `${currentFileDir}`：将图片保存在文件旁边
- `${currentFileDir}/images`：在文件旁边创建 `images` 目录并将图片保存在其中
