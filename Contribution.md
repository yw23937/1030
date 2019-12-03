# 贡献

谢谢您的贡献!

在我们合并您的Pull-Request之前，这里有一些您需要遵循的准则。
这些指导原则的存在不是为了让您烦恼，而是为了保持代码库的整洁、统一以及留作证明。

## 编码标准

这个项目使用 [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) 执行编码标准。
编码标准被定义在这个 **phpcs.xml.dist** 文件里 (存储库的一部分).
该项目遵循教义编码标准v4的一个宽松版本。

您的Pull-Request必须符合上述标准。
要检查代码，可以运行 `vendor/bin/phpcs`. 这个命令将为您的代码提供一个违规列表(如果有的话)。
最常见的错误可以通过运行 `vendor/bin/phpcbf`自动修复。

## 单元测试

请尝试为您的pull request添加一个测试。 这个项目使用 [PHPUnit](https://phpunit.de/)作为测试框架。
您可以通过 `vendor/bin/phpunit`调用来运行单元测试.

## CI

我们会自动运行您的Pull request 通过 [Travis CI](https://www.travis-ci.org)
和 [Scrutinizer CI](https://scrutinizer-ci.com/).
如果您破坏了此测试，我们就无法合并您的代码，
因此，请确保您的代码可以在以上通道运行之前，打开一个Pull request。

## 问题和缺陷

如要创建新问题，可以使用GitHub问题跟踪系统。
请尽量避免使用相关的资源。对于支持相关的问题，请使用更合适的答案的通道和平台
作为问答平台(如Stackoverflow)、论坛、本地PHP用户组。

## 合并

请给我们时间来审查你的Pull request。
我们会尽我们最大的努力尽快的审核每一件事情，但是有些时候也不能全尽如人意。

再次感谢您的贡献!
