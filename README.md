# qqsg_struct

此项目包含了QQ三国的结构体和常见的数据偏移量

## 项目的结构

GameWorld
- Camera
- CurMap
  * GameEntity
    - Speed
    - Status
  
UIRoot
 - children
 - luaEnv
## 说明

有些结构中使用了Unknown 类似的字段，一方面是这些数据很敏感，有人去利于这些做外挂。还有一方面是我自己还没研究出来。

此游戏的近乎所有的战斗逻辑使用的是服务端重演的模式，也就是说不存在增加攻击力、增加防御力、攻击过程变速（提高攻击频率）、无视道具/技能cd的功能。主要是脚本类为主（比如在玩家受控制时自动使用解控技能。）

灵兽系统存在一些bug，如形若坚冰状态在某些情况下无法被移除，这使得玩家全程处于形若坚冰的减伤状态下，从而让其他玩家攻击该玩家时会出现全程的miss/只掉1滴血。目前客户端暂时没有任何途径使用此bug。
