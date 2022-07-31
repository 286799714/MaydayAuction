以下命令用法中，被[]框选的为必填项，被()框选的为选填项。  
注意事项：不要在拍卖会举办期间关闭服务器，拍卖会内的商品不会永久化储存。
###  拍卖行建立步骤
1. 使用WorldGuard插件创建一个region。√  
2. 站在该region内，使用/auction setup enable 使这个region启用为拍卖行。√  
3. 使用/auction setup disable 将该区域取消为普通区域。√
4. /auction setup reserve [金额] 设置该拍卖行加价的底价 √ (例: 当底价为10、起拍价为50时，第一个买家必须以60以上的价格叫价，往后类推。)
5. /auction setup booth 设置展示物品的位置为你的当前位置。√
6. /auction setup await [秒数] 设置从叫价到成交等待的时间。√
7. /auction setup timelimit [秒数] 起拍后无人叫价的最大等待时间。√(例: 当设置为30s时，某物品起拍后30秒无人叫价，则拍卖失败，进行下一件物品的拍卖。)
###  PAPI变量
1. %auction_buyer% 显示当前叫价的玩家的display name。√
2. %auction_bid% 显示当前叫价的金额。√
3. %auction_item% 显示当前拍品的物品名称。√
4. %auction_await% 距离成交的剩余时间。√
5. %auction_timelimit% 无人叫价的剩余等待时间。√
6. %auction_reserve% 加价的底价。√
7. %auction_state% 当前拍卖的状态，可通过修改语言文件来改变内容。√
###  玩家如何参与拍卖
1. /auction action bid (世界名称) (wg区域id) 发起叫价。√输入该指令后，将要求玩家在聊天框内输入一个数值表示叫价的金额。若不满足加价的底价，或玩家的资产不足以支付，叫价将会被驳回。
2. /auction action autobid (世界名称) (wg区域id) 自动发起叫价。√输入后自动为玩家加价，当前叫价+加价底价。
3. /auction manage possess 浏览拥有的拍卖品。可以在此GUI中取回物品。√
4. /auction manage storehouse (世界名称) (wg区域id) 浏览自己上架的物品。√可以在此GUI中上架物品。后面两个参数不输入默认当前所在的拍卖行。
5. /auction manage good (世界名称) (wg区域id)  浏览对应拍卖行正在拍卖的货物。√
###  其他
1. /auction admin start (世界名称) (wg区域id) 使对应的拍卖行开始拍卖。√
2. /auction admin storehouse (世界名称) (wg区域id) 浏览已上架的所有物品。√可以在此GUI中上架物品。后面两个参数不输入默认当前所在的拍卖行。
3. /auction admin cleardrop (世界名称) (wg区域id) debug命令，清除对应拍卖行的残留掉落物。√
###  权限
auction.admin  使用管理员(/auction admin ... 和/auction setup ...)命令的权限。√  
auction.player.limit.x  限制玩家可以上架的物品数量。auction.player.limit.0则为无限制。  
auction.player.common  使用其他非管理员命令的权限。√  