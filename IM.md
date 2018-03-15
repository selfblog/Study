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
    ① key: uid          value: Map<String, String> (sessionId + type => readTime) 128
    ② key: sessionId    value: List<String> (uid)

2. 分表:
    ① 按 sessionId 分表 sessionId uid sessionType readTime
    ② redis:   key: uid   value: List<String> (sessionId)

1000000 * 100keysHash + 1000000 * 10keyList = 1000000 * 4k + 15000000 * 0.04k = 4G + 0.6G = 4.6G

10000 * 100 hash - 672.82K = 40.45M - 672.82K = 40.45M - 672.82/1024 = 40.45 - 0.657 = 39.793 M
100 * 39.793M = 3979.3M = 3.9793G 
10000 * 10 list - 672.94K = 2.46M - 672.94K = 2.46M - 672.94/1024 = 2.46 - 0.657 = 1.803 M
1500 * 1.803M = 2704.5M = 2.7045G

session_status: 152000条数据
其中 不重复uid: 4900个
其中 不重复sessionId: 55700个