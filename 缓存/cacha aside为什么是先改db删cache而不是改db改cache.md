# cacha aside为什么是先改db删cache而不是改db改cache

> 回复史蒂芬曲奇：我的理解 两个请求ab并发改库改cache ，
> db事务顺序a先于b，理想情况下是a的操作结果到cache 而后b再覆盖但是这是不可控的，
> 一个网络抖动b被a覆盖 缓存里就是过期数据了。
> 本质上是一个并发问题，但是delete无所谓
