# PlayerFragment 重构
> 时间：2017-07-14

## 为什么重构？
- PlayerFragment有600行代码，比较复杂
- 不同的逻辑都被放到Fragment中
- 播放器状态不可控，出现放后台继续播放和前台不播放的问题

## 功能
- 数据加载DataLoader的数据承接
    - 接收处理数据
    - 加载更多
    - 错误处理
- 列表事件
    - 滑动变化
    - 页面选择
- 提前缓存播放数据
- 网络变化监听
- 传递评论滑动
- 列表滑动
- 将播放器放进不同的页面
- 空白页面显示
- Fragment生命周期事件
    - onCreateView()
    - onDestroyView()
    - onSaveInstanceState()
    - onCreate()
    - onDestroy()
    - onPause()
    - onResume()
    - setUserVisibleHint()
- EventBus事件监听
    - 视频删除
    - 关注变化
    - 新手引导变化
- 键盘变化监听
- 监听与发送评论列表变化事件
- 设置下拉刷新
- 传递是否输入框与评论列表同步显示
- 打点
    -播放完毕
- 被调用刷新


