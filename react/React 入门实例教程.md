####url:http://www.ruanyifeng.com/blog/2015/03/react.html
1. React.render()
2. jsx < 开始html解析 ，{ 开始js解析
3. 组件 React.createClass({})
4. this.props 与组件的属性一一对应。例外：this.props.children(组件的子节点集)
5. React.findDOMNode 寻找真实DOM节点
6. this.state 可随意改变的组件状态
7. 组件的生命周期
	+ Mounting：已插入真实 DOM
	+ Updating：正在被重新渲染
	+ Unmounting：已移出真实 DOM
8. 通过ajax加载组件数据