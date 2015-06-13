# #TODO 微品金融APP效果优化 #
- 引导页尽量统一背景，用PPT的效果展示出来。
- 由于首页需要加载网络数据，所以会有一个从无数据到有数据的过程。优化这一效果，比如Facebook的效果。
- 首页`viewpager`切换效果调整，避免页面间过大的差距。
- `activity`之间切换时动画效果统一下，比如用`right_in_right_out`效果。
- 标题栏布局封装，启动新页面和返回上一个页面时，首页`viewpager`切换时，尽量保持标题栏不变。[http://stackoverflow.com/questions/7343487/android-viewpager-padding-margin-between-page-fragments](http://stackoverflow.com/questions/7343487/android-viewpager-padding-margin-between-page-fragments)
- 添加`SwipeBack`效果，尽量保持拇指的位置不变就可以完成交互。[http://stackoverflow.com/questions/19105400/swipe-back-like-pinterest-or-tumblr](http://stackoverflow.com/questions/19105400/swipe-back-like-pinterest-or-tumblr)
- `webview`展开的页面做好响应式适配，比如图片宽度，比如页面样式。
- 节约手机空间，尽量保持单手、拇指操作习惯，布局上做好调整，保守一点采用流式布局。
- APP框架上适当重构，首页和详情页的多次重复请求数据，考虑mvp设计思路来简化activity中代码。