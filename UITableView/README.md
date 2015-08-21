### Terminating app due to uncaught exception 'NSInternalInconsistencyException', reason: 'Auto Layout still required after executing -layoutSubviews. UITableView's implementation of -layoutSubviews needs to call super.'
#####           这个问题在iOS7直接就是崩溃了，在iOS8上没什么问题。搜索后的解决方法是关闭AutoLayout，但我要用AutoLayout。在Stack Overflow上找到这个：
[解决方法](http://stackoverflow.com/questions/12610783/auto-layout-still-required-after-executing-layoutsubviews-with-uitableviewcel)
不过我出现问题的地方不一样，我是因为给tableFooterView加上了Constraints后崩溃的，不过原因应该是一样的。按给出的问题提示是UITableView的了类没有调用super layoutSubviews，但我并没有继承UITableView，所以也并不知道是什么情况。
