# Basic-project-structure

一个通用的基础架构示例

## 基本项目构成

<!-- https://mermaid.js.org/ -->

```mermaid
graph LR;

    classDef red fill:#600
    classDef green fill:#030
    classDef yellow fill:#303

    BR1(bps-contractor-entry \n 包网 - 入口1):::yellow
    BR2(bps-contractor-entry \n 包网 - 入口2):::yellow
    BQ[bps-contractor-h5 \n 包网 - 前端]
    

    FZ([Load Balance \n 业务集群 负载均衡]):::green
    CDN([CDN \n 内容分发网络]):::green
    API{{bps-core-api \n 核心 - API}}:::red


    subgraph 包网
        用户 --> BR1 --> BQ
        主代理 & 子代理 --> 代理
        承包商 & 代理 & 业务员 --> BR2
        BDB[(包网数据库)]
    end
    BR2 -.-> CDN
    BQ -.-> FZ


    subgraph 总台
        CDN --> bps-manager-contractor\n承包商-管理后台 & bps-manager-agent\n代理-管理后台 & bps-manager-salesman\n业务员-管理后台 --> FZ --> API
        CDB[(核心数据库)]
        超管 & 财务 & 运营 --> bps-manager-main\n总台-管理后台 --> API
    end
    API -.-> BDB & CDB
```

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
