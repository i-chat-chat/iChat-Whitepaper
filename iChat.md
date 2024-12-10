# 区块链聊天系统计划书
## 1. 概述
    本系统旨在通过区块链技术提供一个去中心化的聊天平台，用户可以无需身份认证即可实现点对点加密聊天，同时拥有钱包功能。
    用户之间的聊天内容只有拥有者才能解密，且所有的消息都具备阅后即焚功能，确保通信内容的安全性和隐私性。系统还集成了代币经济机制，
    使用 iChat 代币 激励用户和服务者之间的互动。

## 2. 系统架构
###   2.1 用户角色
       权限与安全：用户通过助记词（mnemonic phrase）获得系统权限。助记词一旦丢失，用户将无法恢复访问权限，因此必须妥善保管。
       消息加密：所有消息在传输过程中都使用端到端加密，只有发送者和接收者能够解密消息内容。
       消息存储：系统仅保存未读消息的 6小时，超过时间则自动丢弃，已读消息即使丢弃，确保阅后即焚的隐私保护。
       离线处理：如果用户在发送消息时处于离线状态，消息将直接丢弃，无需等待接收。
###   2.2 服务角色
       服务角色是系统中的节点，主要负责消息传输和验证服务。每个服务角色持有一定数量的 iChat 代币，并提供服务供其他用户使用。

        iChat 代币要求：成为服务角色需要持有至少 一百万枚 iChat 代币，这是为了确保服务角色的稳定性与激励机制的实施。
        服务注册与发现：服务角色之间需要进行相互注册，互相验证节点是否合法，确保每个服务节点都能获得最新的在线服务角色列表。此机制可确保服务角色能够连接到其他有效服务节点。
        消息传输与查询：服务角色提供接口供用户查询是否有新的消息，同时提供当前在线服务角色的列表，以便用户选择最佳的连接服务节点。
        用户角色与服务端的连接：
        用户在发送消息时需要连接至少 5个 服务端，以确保消息能快速并且安全地到达目标。
        每个用户至少需要同时连接 5个以上的服务端，这样可以确保系统对未读消息的监控更加可靠。
### 2.3 奖励与惩罚机制
    服务角色的存在与贡献需要通过代币激励来支持，确保系统的长期运作和活跃度。
    
    奖励机制：
    
    成为服务角色的用户可以通过提供服务获得 iChat 代币奖励。每提供 1小时的服务，系统会根据服务时长发放对应数量的代币。
    奖励会在用户完成 1小时服务后自动发放，奖励不满1小时的服务时段将不予发放。
    惩罚机制：
    
    服务质量不达标的服务角色将被系统标记并减少其 iChat 代币奖励。包括但不限于：连接延迟过高、消息丢失、系统崩溃、频繁上线下线等行为。
    代币流通与激励：通过服务角色与用户角色的交互，iChat 代币将在系统内进行流通。用户在发送消息时，也可以根据连接的服务节点数量支付一定数量的代币，作为对服务角色的奖励。

### 3. 技术实现与安全保障
   #### 3.1 区块链技术
    本系统将基于 区块链 技术构建去中心化的聊天与服务网络。所有交易记录、代币流转、以及用户消息都将在区块链上进行加密存储，保证数据的不可篡改性与透明性。

   #### 3.2 加密通信
        端到端加密：所有用户间的消息都通过对称加密和公私钥加密技术进行加密，确保只有通信双方能够解密并读取消息内容。
        私钥管理：用户的私钥和钱包数据将通过本地加密方式存储，防止泄露。用户必须通过助记词进行恢复和授权。
        3.3 激励与经济模型
        iChat 代币将在系统内形成激励机制：
        用户奖励：用户角色通过发送消息和参与网络活动（如验证交易、消息传播等）获得代币奖励。
        服务奖励：服务角色根据服务时长和质量获得代币奖励。
        代币流通：iChat 代币不仅作为系统内的激励，还可以在交易所上进行流通交易，提供多元化的经济模型。
   #### 4. 未来发展方向
       扩展更多功能：随着用户需求的增长，系统可以集成更多的功能，如群聊、语音聊天、视频聊天等。
       跨链集成：未来可以考虑将系统与其他区块链平台集成，提供更多的代币支持和跨链功能。
       增强隐私保护：通过引入更加先进的加密技术和协议，进一步提高用户隐私和安全保护。
### 4. 未来发展以及盈利模式
        1.当一定用户规模,代币价值会逐步上升,这是早期投资者盈利模式之一
        2.用户足够多,在客户端软件上引入一些商业广告,盈利用来购买代币,并销毁。
        3.更多模式等待开发中

### 5. 时间线
        dome版本上线: 2025.1.10
        正式版本上线: 2025.2.10
        

    