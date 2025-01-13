# AiGoChecker
我们经常遇到代码审计需求，我们有很多选择比如开源codeql、商业fortify，但是往往审计不出什么漏洞出来。

这时候就需要人工审计，而人工审计主要依靠crtl+f或者全局shift+ctrl+f去搜，耗费精力时间。

为了辅助人工审计，于是开发了一系列的代码审计工具（JavaChecker、PhpChecker、GoChecker），最近将GoChecker重构，使用AST语法树做分析，并且结合AI强（有点类似“seay源代码审计系统”，但是比seay源代码审计系统增强了许多）。

优化功能
* AI助力：结合AI识别Sink函数，进一步增强审计能力
* 使用简单：无需安装Golang环境，开箱即用，对缺少依赖库或者残缺的项目仍然可以审计成果，突破了环境限制的束缚。
* 优化展示：与VSCode深度结合，实现了代码高亮显示，提升了开发体验。
* 追踪分析：借助AST（抽象语法树）分析技术，并进行了基础的数据流分析，增强了代码追踪与分析能力
* 代码安全：不开启AI功能，不会将代码内容上传到云



# 演示

```
GoChecker -path code_project -key sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```


https://github.com/user-attachments/assets/51339ef0-f42a-4f61-b7ff-c9a4d588b515




<img width="1589" alt="image" src="https://github.com/user-attachments/assets/dee1ea0d-eddb-4ab1-a8ad-d819cb9b98fa" />


注意：目前只支持阿里云的百炼sk，不加-key参数则不会开启ai
