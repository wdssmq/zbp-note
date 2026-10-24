## cSpell - VSCode 插件

### 插件地址

Code Spell Checker - Visual Studio Marketplace

[https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker "Code Spell Checker - Visual Studio Marketplace")

### 有啥用

帮你在 VSCode 中检查英文拼写错误，虽然是弱提醒。

### 使用姿势

一些拼接变量或者特殊命名需要保留然后让插件不要报错，可以对其进行配置；

```json
{
	"settings": {
		"cSpell.words": [
			"blogpath"
		]
	}
}

```

## intelephense - VSCode 插件

### 插件地址

PHP Intelephense - Visual Studio Marketplace：

[https://marketplace.visualstudio.com/items?itemName=bmewburn.vscode-intelephense-client](https://marketplace.visualstudio.com/items?itemName=bmewburn.vscode-intelephense-client "PHP Intelephense - Visual Studio Marketplace")

### 常用变量

```php
/** @var array $lang */
/** @var object $zbp */
/** @var string $blogpath */
```

## 让 copilot 按指定的规则生成提交信息

```json
{
	"github.copilot.chat.commitMessageGeneration.instructions": [
		{
			"file": ".github/rule-for-git.md"
		}
	]
}
```
