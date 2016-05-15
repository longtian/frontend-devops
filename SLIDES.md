class: middle, center

### CloudInsight
## 前端 DevOps 实践经验

王龑

???

- 谢谢主办方和场地提供, 谢谢朋友们
- 我是谁
- 我来自哪里
- 我在做什么
- 我今天要分享的东西
---
class: middle, center

# 文化

---

# 明确 DevOps 的目的

- 促进软件的开发, 按时交付
- 关注过程、工具
- 强调开发、运维和测试的紧密合作

也就是:

- 不加班
- 不重复
- 多职能

---

# 引入和形成自己的开发模式

- 严格控制例会时间
- 演示自己的成果
- 公开的代码审查
- 发布完后的反思会

---
class: middle, center

#  <q> 吃自己的狗食 </q>

---

# 拥抱变更而不是频繁的改需求

- 对创业公司来说, 快速变更简直就是生命
- 封闭的冲刺迭代

---
class: middle, center

# 环境

---

# 保持开发环境和线上环境等价

> 使用 `package.json` 显示地声明依赖

开发环境操作系统

- `Linux`
- `Mac`
- `Windows`

持续集成环境

- `Linux`

\* 在基础设施(仓库, 网络)完善的情况下尝试 `Docker`

---

# 使用 `GIT` 管理源代码

> 打不死的小强, 删不掉的代码

1分钟读懂分支管理:

- feature/*** 分支
- development 分支
- master 分支
- hotfix/*** 分支

---

# 快速创建开发环境

|     场景             |   建议                      |
|----------------------|----------------------------|
|相同型号的老机器比较多   | `Ghost` 系统               |
|机器少,但是性能强劲     | `VirtualBox` 或者 `ESX`    |
|预算有限, 运维少        | 青云, 阿里云                 |
|预算充足, 运维强        | 自建集群,内部的 IaaS 系统     |



---
class: middle, center

# 开发

---

# 升级你的 Node.js 版本

跟随语言的发展, 选择 Node.js LTS 版本, Node.js V6.1 对 ES2015 的支持度已经达到了 95 %

前端项目和后端项目的界限正在模糊。

---

# 使用 JavaScript 语言转换器

> ES 2015, ES 2016

- 抛弃古董浏览器
- 写明天的代码, 同时兼容现代浏览器
- 使用垫片技术兼容

工具

- babel

---

# 使用 ESLint 做代码规范

- 先解决有还是没有的问题
- 在解决合理还是不合理的问题

*ESLint 前*
```
return <Component
 onClick={ this.handleClick.bind(this) }
 className='class-1'/>
```

*ESLint 后*
```
return (
  <Component
   className='class-1'
   onClick={ this.handleClick.bind(this) }
  />
);
```

---

# 使用打包工具

遵循 `单一职责` 和 `开闭原则` 等, 尽情地去新建 `JS` 文件,
因为最后都会被压缩到一个文件里。

打包工具:
- webpack
- browserify

---

# 保障 DevOps 的安全

- 服务器启用 HTTPS
- 开发环境尽量使用 SSH 证书, 并开启密码保护
- 做好监控和安全防护

---

# 基于 Jenkins 使流程自动化

以下流程都可以自动化

- 安装环境依赖
- 代码静态检查
- 单元测试
- 编译打包
- 线上部署和验证
- 邮件通知

---

class: center, middle

[图]

---

class: middle, center

# 运维

---

# 引入可靠的 CDN 技术

好处显而易见:

- 前端静态资源几乎不需要服务器管理人员。
- 存储非常便宜, 持续部署, 动态切换

`CloudInsight` 相关数据

---

# 使用 Hash 解决缓存问题

**源文件**

`app.js`

**MD5**

`app-1w4j5ut9.js`

**Commit**

`app-fe34ftr0.js`

**Webpack**

`app-i2fedisu.js`

**Tag**

`app-v5.2.1-hoxfix-1.js`

---
class: middle, center


---

# 监控

---

# 去逛逛 DevOps 的 SaaS 商店

.badge[基础设施]

阿里云, 青云 , AWS

.badge[项目管理]

Github, Jira, Teambition

.badge[聊天工具]

BearyChat, Slack

.badge[应用程序监控]

OneAPM

.badge[平台和服务监控]

Zabbix, CloudInsight

.badge[用户体验监控]

OneAPM BI

.badge[运营]

Google Analaytics, 百度统计, GrowingIO

