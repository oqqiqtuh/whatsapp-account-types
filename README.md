# whatsapp账号有几种、怎么开：个人号、Business 应用、开放平台与官方业务账户怎么区分？开通条件、号码与模板限制一次讲清（附账号类型对照表）

WhatsApp 账号不是一个东西。你搜“whatsapp账号”，大概率落在三类需求里：想注册一个自己用；想做跨境生意，搞清楚 Business 账号怎么开；或者看到别人的账号名后面带认证徽章，想知道怎么才能拿到。先把结论放前面：小生意日常回消息，下载免费的 WhatsApp Business 应用就够用；需要 API、模板消息、多个号码统一管理，才用得上 WhatsApp Business 开放平台；那个认证徽章叫官方业务账户（Official Business Account），是开放平台之上的认证，不是一种套餐，也没有“花钱加急”的官方通道。

下面把四类账号的分工、官方开户路径、以及最容易踩坑的数量限制讲清楚。这些数字，多数中文教程只讲到“注册”就停了。

## 你需要的是哪一种账号

把“WhatsApp 账号”当成一个整体去搜，容易在错误的方向上花时间。按场景对号入座更省事：

> - 一个号码、一个小店、每天手动回几十条消息，不需要对接系统 → **WhatsApp Business 应用**，免费下载，注册即用。
> - 要做自动回复、模板群发、客服系统对接，或者一组号码集中管理 → **WhatsApp Business 开放平台**，先分别创建 WhatsApp account（WAAC）和 Messaging account。
> - 想在主页和聊天标题显示认证徽章 → 满足条件后申请**官方业务账户**，注意 Business 应用用户不能申请。
> - 如果你只是想有一个海外号码来接收 WhatsApp 验证码，第三方海外数字账号商城（比如下文提到的账号星球）是一个选择，但它卖的是海外手机卡和相关账号资源，官方 WhatsApp 账号本身仍需自己注册。

👉 [查看当前可用的 WhatsApp Business 开户与海外号码方案](https://accboyytbetw.acceboy.com/)

## 四类账号对照：面向谁、要不要钱、能不能认证

| 账号类型 | 面向谁 | 是否收费 | 能否申请认证徽章 | 关键限制 |
| --- | --- | --- | --- | --- |
| WhatsApp Messenger 个人账号 | 普通个人用户 | 免费 | 不适用 | 与 Business 应用不能共用同一号码 |
| WhatsApp Business 应用账号 | 小型企业、个体经营者 | 免费下载 | **不能**，官方业务账户不适用于 Business 应用用户 | 业务类别最多选三个，不能自定义类别 |
| 开放平台 WhatsApp account（WAAC）+ Messaging account | 使用 API 的商家、解决方案提供商 | 平台按消息计费，费率与类目、市场相关 | 可以 | 两类账户必须都有，否则收发消息和管模板都无法工作 |
| 官方业务账户（OBA） | 已在开放平台运营的商家 | 认证本身不单独收费，使用平台按规则计费 | 就是徽章本身 | 需完成公司验证或满足消息量要求，且注册满 30 天 |

官方资料并没有给出一个“全平台统一价”。WhatsApp Business 平台的计费按已送达消息、消息类目和市场费率计算，费率会随市场和类目变化，具体金额以你后台的 Messaging account 账单为准。这一点后面会展开。

## WhatsApp Business 应用：免费，但有三件事要先知道

WhatsApp Business 是一款可免费下载的应用，专为小型企业打造。注册流程本身不复杂，麻烦的是下面这三条，很多教程不讲。

第一，同一个电话号码无法同时关联 WhatsApp Messenger 和 WhatsApp Business。你可以同时用两个应用，但它们必须绑不同的号码。想“一个号两用”行不通。

第二，聊天记录可以迁移。已有 Messenger 账户的用户，可以把账户连同聊天记录和影音内容迁移到 Business 应用；反过来，停止使用 Business 应用时，也可以把账户和聊天记录转移回 Messenger。

第三，业务类别最多选三个，且无法创建自定义类别。创建业务主页时，你只能从推荐类别里挑，或者点“+ 查看更多类别”去探索，但不能自己写一个类别名。对做细分行业的商家来说，这一点会限制主页展示的准确度。

创建主页的流程依次是：输入商企名称、选业务类别（最多三个）、添加营业时间、添加头像、填业务地址和网站链接（可跳过）、写业务概述（可跳过）。业务概述那一栏可以用 Meta AI 业务助手生成多个版本，选一个或继续生成，之后还能随时编辑。

如果你的业务已经开始需要自动回复、模板消息、多客服协作，官方文档里的一句提示值得记下：希望增强业务体验的商家，应当考虑使用 WhatsApp Business 开放平台。这两者不是升级版和普通版的区别，是两套不同的账户体系。

## 开放平台账户：WAAC 和 Messaging account 分工不同，缺一不可

这是近两年变化最大、也最容易被旧文章误导的部分。WhatsApp Business 开放平台使用两种账户类型：

- **WhatsApp account（WAAC）**：持有一个业务电话号码，代表商家在 WhatsApp 上的存在。
- **Messaging account**：持有消息模板和账单信息。每个与你合作的伙伴有各自的 Messaging account。

收发消息、创建和管理模板，两类账户都需要。只共享其中一类，消息功能不会工作——WAAC 提供发送用的业务电话号码，Messaging account 提供模板和付款方式。

账号模型正在演进，几个变化需要知道：

- 现有的 WABA ID 现在标识的是 Messaging account，ID 值和 `waba_id` 字段名都没变，已有调用无需修改。
- WhatsApp account ID 会在后续阶段推出。
- On-Behalf-Of（OBO）Messaging 账户所有权模式已经弃用，不再可行。

如果你看的教程还在讲“一个 WABA 对应一个号码和一套模板账单”，那是旧模型，不能直接照搬。

### 三条创建路径

**通过 App Dashboard（Cloud API）**：完成 Cloud API Get Started 步骤后，你会得到一个测试 WhatsApp account、测试 Messaging account 和测试业务号码，并能访问 App Dashboard > WhatsApp > API Setup 面板。在该面板添加正式业务电话号码后，会生成包含该号码的 WhatsApp account，以及用于模板和账单的 Messaging account。

**通过合作方**：合作方会提供指引，通常要完成 Embedded Signup 流程，收集企业信息并生成两类账户，然后用合作方的应用访问新账户及相关资产。

**通过 Meta Business Suite**：适合那些通过 Meta Business Suite 而非 Cloud API 提供服务的合作方。创建 WhatsApp account 的路径是：进入 business.facebook.com，创建或选择业务资产组合，打开设置（齿轮图标）> 账户 > WhatsApp 账户，点蓝色“+添加”，选“Create a new WhatsApp account”，完成流程。创建 Messaging account 走同一入口下的 Messaging accounts 面板，选“Create a new Messaging account”。

顺带说一句，Meta Business Suite 添加账户还有一条限制：只有 WhatsApp Business 业务账户能添加到业务资产组合，每个账户只能属于一个业务资产组合，且你必须对资产组合有完全控制权。如果设置里看不到“WhatsApp 账户”，多半是没有完全控制权。

## 限制清单：号码、模板、共享，这几组数字最影响决策

前排文章讲开户的多，讲限制的少。下面这几组数字，直接决定你的多号码、多团队方案能不能落地。

**模板上限与业务资产组合验证状态挂钩。** 组合未验证时，每个 Messaging account 最多 250 个消息模板；组合已验证，且至少一个 WhatsApp account 的业务电话号码有已批准的 display name，每个 Messaging account 最多可到 6,000 个。差了 24 倍，验证状态值得提前处理。

**号码和层级都有初始上限。** 每个业务电话号码映射到一个 WhatsApp account；WhatsApp account 可以链接成 WhatsApp account hierarchy，把一组号码当整体管理。Meta Business Account 最初每个 hierarchy 限 2 个注册业务电话号码，这个上限可提高到 20 个；最初限 20 个 WhatsApp account hierarchy。

**归属唯一，不能跨企业迁移。** 一个 WhatsApp account 或 Messaging account 只能属于一个业务资产组合，不能由两个或更多组合共同拥有。Messaging account 的时区和币种在附加信用额度后不可编辑，也不能从一个企业迁移到另一个企业。开户时选错时区或币种，后面改不了。

**共享给合作方有两组上限。** 共享 WhatsApp account 会让合作方访问其中的业务电话号码，最多可共享给 5 个 Solution Partner；共享 Messaging account 会让合作方访问模板和账单信息，最多可共享给 2 个合作方。两类账户必须都共享，只共享一类消息功能不工作。

**合作方权限需要 Advanced access。** 合作方应用对每项使用的权限都需要 Advanced access：`whatsapp_business_management` 没有 Advanced access 时，API 调用会返回错误码 `200`；`whatsapp_business_messaging` 用于从业务电话号码发送消息、接收消息和状态 webhook。如果合作方是 Solution Partner（有信用额度），对方必须先与你共享其信用额度，你才能用其应用发消息。

**违规通知通过 webhook 推送。** 订阅 `account_update` webhook，可在账户状态变化时收到通知，包括违反政策和条款的情况。webhook 订阅由 Messaging account 持有。违规通知里会带 `phone_number`、`event: ACCOUNT_VIOLATION` 和 `violation_info.violation_type`。这条对做自动化监控的团队有用。

## 官方业务账户：认证徽章，不是花钱能买的套餐

官方业务账户的作用，是让使用 WhatsApp Business 开放平台的商家在主页和聊天对话标题中显示认证徽章。它不是一种套餐，也不是 Business 应用用户能申请的状态。

申请前要满足两条前置条件中的至少一条：完成公司验证，或者展示在连续 30 天内进行至少 1,000 次对话的发送优质消息记录。同时，商家必须在 WhatsApp Business 开放平台注册至少 30 天。

申请步骤：前往 Meta Business Suite，选择业务资产组合，点所有工具，点 WhatsApp 管理工具，在 WhatsApp 账户版块找到并点击要申请的电话号码，在个人主页版块找到官方业务账户并点提交申请。如果没有为电话号码设置两步验证，必须先启用两步验证，这是硬性前置步骤，没完成就无法提交。之后输入所需信息并提交。

审核后会收到通知。如果被拒绝，可在 30 天后重新提交申请。

官方明确不授予官方业务账户的对象有三类：企业工作人员、测试账户、WhatsApp Business 应用用户。最后一条的原因写得很直白：Business 应用用户未被要求完成公司验证，所以不适用。市面上那些“快速认证”“包过绿勾”的服务，和这套官方条件对不上，看到时多留个心眼。

## 账户中心：自愿添加，但信息边界要想清楚

如果你用的是个人 WhatsApp，可能会遇到“账户中心”或“Meta 账户设置”的提示。这两者是同一个东西的不同叫法，页面正在逐步推出，你看到哪个都不奇怪。

添加 WhatsApp 到账户中心是完全自愿的，可以随时添加和移除，不添加也能照常使用 WhatsApp。添加后能解锁一些跨应用体验，比如把 WhatsApp 动态分享到 Facebook 或 Instagram 快拍，一站式管理某些账户设置。

隐私边界有两条要说清楚：添加账户中心不会影响 WhatsApp 私人消息或通话的端到端加密，WhatsApp 和 Meta 也看不到听不到；不会与其他 Meta 旗下公司分享联系人名单。

但添加之后，信息共享范围会扩大。WhatsApp 会额外收集设备和连接信息（例如每次使用账户中心内 WhatsApp 时创建的唯一编号）以及使用情况和日志信息。其他 Meta 旗下公司会获得你的电话号码、WhatsApp 头像、年龄信息（如已提供）、分享到快拍的动态内容、应用版本或设备语言、使用情况和记录信息等。这些信息会被用于在 Meta 旗下产品上展示广告时定制个性化广告体验并衡量广告表现。

撤回方面：从账户中心移除 WhatsApp 后，Meta 会在 7 天内停止整合 WhatsApp 账户和账户中心其他账户的信息；移除前已经整合的信息会保持整合状态。

还有一个容易被忽略的历史条款：如果你在 2016 年选择了不与 Meta 分享 WhatsApp 账户信息用于改善 Meta 广告和产品体验，那么把 WhatsApp 账户添加到账户中心，意味着你同意分享这些信息，也同意账户中心相关的所有信息分享行为。

## 常见问题

**同一个号码能同时用 WhatsApp 和 WhatsApp Business 吗？**
不能。可以同时使用两个应用，但二者必须关联不同的电话号码，同一号码无法同时关联这两个应用。

**Business 应用用户能申请认证徽章吗？**
不能。官方业务账户不适用于 WhatsApp Business 应用用户，因为他们未被要求完成公司验证。

**一个营业执照能开几个业务号码？**
Meta Business Account 最初每个 WhatsApp account hierarchy 限 2 个注册业务电话号码，可提高到 20 个；最初限 20 个 WhatsApp account hierarchy。实际能开多少还受业务资产组合和验证状态约束。

**WABA ID 还能用吗？**
能。现有 WABA ID 现在标识 Messaging account，ID 值和 `waba_id` 字段名都没变，已有调用无需修改。

**开放平台的计费怎么算？**
按已送达消息计费，费率和消息类目、市场相关，具体金额以你 Messaging account 后台账单为准。官方没有给一个全平台统一价。

**我在国内，注册 WhatsApp 收不到验证码怎么办？**
这是号码可达性的问题，不是账号类型的问题。官方渠道不提供号码，需要你自备一个能接收验证码的海外号码。第三方海外数字账号商城在这类场景下是常见选择，但注意它们提供的是号码或相关账号资源，WhatsApp 账号本身仍要通过官方应用或开放平台注册。

## 下单或开户前，最后确认两件事

第一，确认你要的号码没有注册过 WhatsApp。一个号码对应一个账号，已经绑定过的号码不能重新注册，这一点在买号或换号前必须先问清楚。

第二，确认你的业务资产组合是否已经完成验证。模板上限从 250 到 6,000 的差别，就卡在组合验证和 display name 审批这两步上，早做早省事。

按需求最后给一次判断：只要一个免费的小生意号，下载 WhatsApp Business 应用；要 API、模板消息、多号码统一管理，走开放平台，先把 WAAC 和 Messaging account 都建好；要在主页和聊天标题显示认证徽章，先满足公司验证或 30 天 1,000 次对话的条件，再提交官方业务账户申请。需要海外号码或相关海外账号资源，可以对照自己的场景挑，别把第三方资源和官方账号混为一谈。

👉 [需要海外号码或相关海外账号资源，可以从这里开始看](https://accboyytbetw.acceboy.com/zh-cn-cny/buy-sim-card-topup)
