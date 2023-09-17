# Basic-project-structure

一个通用的基础架构示例

## 基本项目构成

<!-- https://mermaid.js.org/ -->

```mermaid
graph TD
    A([basic-project])
    A --应用服务中心--- center["center\n项目后端，负责提供 api、rpc 等服务"]
    A --项目开发工具包--- sdk["sdk\n开发工具、脚手架、后端生成的开放文件"]
    A --管理后台--- manager[manager]
    A --客户端--- client[client]

    center --go 服务端--- go[center-go]
    center --php 服务端--- php[center-php]

    client --手机 H5 客户端--- clientMobile[client-mobile]
    client --Android 客户端--- clientAndroid[client-android]
    client --iOS 客户端--- clientIOS[client-ios]
    client --Flutter 客户端--- clientFlutter[client-flutter]
```

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
