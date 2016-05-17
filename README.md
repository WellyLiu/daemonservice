# daemonservice
Android App keep alive

1. Android 对APP的生命周期有自己的一套管理方法.
2. 优先级 + 消耗内存; 当内存low到指定值,则扫描对应优先级的APP,优先kill消耗内存多的.
3. 进程优先级参数  oom_adj
4. 当前显示进程高于前台进程优先级高于后台进程.  手机系统中电话进程oom_adj为负数,优先级最高,永远不会被oom杀掉.
5. 常规下,一个APP一个进程,当进程被OOM kill时, UI,Service是有先后优先级被kill的.
