###源url:http://es6.ruanyifeng.com/

###变量
1. 变量let
	+ 块级变量
	+ 不存在变量提升
	+ 绑定区域
	+ 不允许重复声明
2. 常量const
	+ 与let相似
	+ 常量对象属性可以添加（可以用Object.freeze冻结）
	+ 通过import export 的跨域常量
3. 能通过var声明全局变量 let+const不行

###变量的解构赋值
1. 数组的解构赋值
	+ var [a,b,c]=[1,2,3] 
	+ 当赋的值不严格等于undefined，解构失败
	+ 解构从左到右，右边缺失，左边仍能正确解构
	+ 支持嵌套
	+ 可以指定默认值 var [a=1]=[null]//a为1
2. 对象的解构赋值
	+ var {key1,key2}={key1:"value1",key2:"value2"}
	+ 当变量名与属性名不一样时：var {key:var_name}={key:"value"}
	+ 当赋的值严格等于undefined，解构失败
	+ 支持嵌套与默认值
	+ 对象解构小心与块作用域弄混
3. 字符串的解构赋值
	+ 单个字符 var [a,b,c]="key" //a-k,b-e,c-y
	+ length var {length}="key" //length 为 3
4. 函数参数的解构赋值
	+ 变量解构的默认值与函数参数的默认值要区分好
5. 括号会影响解构赋值
	+ 不能使用括号的情况
		- 变量声明语句
		- 函数参数（也属于变量声明）
		- 模式或模式的一层不能放在括号中
	+ 可以使用括号的情况
		- 赋值语句（非变量声明）

6. 好用的地方
	+ 交换变量
	+ 函数参数赋值+默认值+返回值的快速获取
	+ json数据 获取
	+ Map 数据获取
	+ 模块数据 获取

###字符串的扩展
1. codePointAt() 支持4个字节 charAt只支持2个字节
2. String.fromCodePoint() 与 String.fromCharCode()
3. at() 与 charAt()
4. Unicode表示字符
	+ \u{20bb7} 可以表示2与4字节的字符

5. 正则表达式u模式
	+ 识别正则表达式中Unicode表示字符
	+ 识别4字节的字符
6. 正则表达式y模式
	+ 匹配从第一个开始，g模式则随处开始
	+ sticky属性,判断正则表达式是否设置了y模式
7. normalize()不太懂
8. 新方法
	+ includes(str) 是否包含str
	+ startsWith(str) 在开头是否有 str
	+ endsWith(str) 在结尾是否有 str
	+ 以上都支持第二个参数，位置指定
	+ repeat() 字符串重复
9. 模板字符串
	+ ``开头结尾，自带 变量+多行
	+  模板函数 tag(strs,...values) strs字符串数组，values变量数组
	+  调用 tag \`模板字符串 \`

10. String.raw() 斜杠自动被转义