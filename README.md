# 踩坑记录

1. 用git保存好（至少保存在本地）。 经常改了部分东西之后发现以前工作的好好的代码突然不起作用了，可能是一些很简单的错误，但是找问题浪费了大量的时间。

2. 当修改不起作用时检查文件修改后是否保存了（由于每次保存都会热部署，所以有时候改动多的时候忘了保存，然后切换文件后编译发现改动不生效）。 hbuilder 中未保存的文件会有*号在tab前

3.  （? export const 不起作用，暂时未知）

4. uni.navigationto  不在前面带”/“会默认带上当前路径

5. 下拉刷新需要在pages.json 中配置

6. 同时使用浏览器和真机做调试。 chrome有vue的插件，能够更好地定位问题。 而真机可以看兼容性问题。如果只有其中一个有问题，还可以探寻真机的webview和浏览器的区别。

7. view （div）当内容多时自己会撑开，不需要scrollview也能实现滚动。 如果在view中嵌入scrollview，需要保证view的高度不是自动撑开的。

8. div 的position如果不是static，那么其宽度的默认值不是100%

9. $ref在app中是不起作用的。 具体原因待探究，猜测因为app没有dom节点？需要验证

10. app内打开无法使用safari 开发工具做调试。
