## im_session_status查询场景梳理


####

1. 查询自己与对方的已读时间          sesssionId in 查询
2. 查询用户会话                     uid 查询
3. 更新用户会话已读时间              sessionId, uid, readTime 更新

一张表, 会话扩散, 性能降低
####

####
方案:
1. 使用其他存储方式:  如 redis  
    ① key: uid          value: Map<String, String> (sessionId => readTime)
    ② key: sessionId    value: List<String> (uid)

2. 分表:
    ① 按 uid 分表
    ② redis:   key: sessionId   value: List<String> (uid)
