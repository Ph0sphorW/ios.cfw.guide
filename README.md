## ios.cfw.guide
完整的 iOS 越狱指南，自崭新出厂到完全越狱。

https://ios.cfw.guide/

本分支作为中文本地化仓库使用。由于上游迟迟不对中文文档进行翻译批复，故本人开启此仓库以进行个人翻译。

## 本地运行

你需要在你的系统上安装如下软件:
- [Node.js v12+](https://nodejs.org/)
- [Yarn v1 classic](https://classic.yarnpkg.com/en/) (npm install --global yarn)

如需本地测试运行此网站，请运行如下命令:
```
git clone https://github.com/Ph0sphorW/ios.cfw.guide/.git --recursive
cd ios.cfw.guide
yarn install
yarn dev
```
以将 Markdown 文件转译为 HTML 并在 http://127.0.0.1:8080 上运行本地服务器。

## 构建网站

遵循以上步骤，在最后一步改为执行 `yarn build`。完成之后输出结果将会储存在 `/docs/.vuepress/dist`。

## 翻译本站

如需帮助 ios.cfw.guide 本地化，请到其 [Crowdin project](https://crowdin.com/project/ioscfwguide) 进行翻译而不是在上游仓库打开拉取请求。

如需帮助本仓库进行翻译，请直接 PR，无需使用 Crowdin。
