## im_session_status查询场景梳理


####

1. 查询自己与对方的已读时间          sesssionId in 查询
2. 查询用户群                       uid isGroup 查询
3. 更新用户会话已读时间              sessionId, uid, readTime 更新
4. 建立会话                         多条插入

一张表, 会话扩散, 性能降低
####

####
方案:
1. 使用其他存储方式:  如 redis
    ① key: uid          value: Map<String, String> (sessionId + type => readTime)
    ② key: sessionId    value: List<String> (uid)

2. 分表:
    ① 按 sessionId 分表 sessionId uid sessionType readTime
    ② redis:   key: uid   value: List<String> (sessionId)

1000000 * 100keysHash + 1000000 * 10keyList = 

session_status: 152000条数据
其中 不重复uid: 4900个
其中 不重复sessionId: 55700个