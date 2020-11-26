### jQuery 操作元素尺寸 `三套方法, 四种使用方式`
   1. **width() 和 height()**
   + 语法:
     元素集合.width()
     元素集合.height()
   + 获取:
      元素的 内容区域 的尺寸
      => 注意: 是不是占位都能拿到, 拿到的一定是 内容区域
   2. **innerWidth() 和 innerHeight()**
   + 语法:
     元素集合.innerWidth()
     元素集合.innerHeight()
   + 获取:
     元素的 内容区域 + padding 的尺寸
   3. **outerWidth() 和 outerHeight()**
   + 语法:
      元素集合.outerWidth()
      元素集合.outerHeight()
   + 获取:
      元素的 内容区域 + padding + border 的尺寸
   4. **outerWidth(true) 和 outerHeight(true)**
   + 语法:
      元素集合.outerWidth(true)
      元素集合.outerHeight(true)
   + 获取:
      元素的 内容区域 + padding + border + margin 的尺寸
### 创建节点
   + $(HTML格式字符串)
    - console.log($('<div></div>'))
    - $(一个选择器) 表示获取元素
    - $(一个 DOM 元素) 表示把 DOM 元素转换成 jQuery 元素集合
    
### 插入节点
   + 内部插入(父子关系的插入)
    1. append() `在爸爸孩子的最后`
    - => 父节点.append(要插入的子节点)
    2. appendTo() `在爸爸孩子的最后`
    - => 要插入的子节点.appendTo(父节点)
    3. prepend() `在爸爸孩子的最前面`
    - => 父节点.prepend(要插入的子节点)
    4. prependTo() `在爸爸孩子的最前面`
    - => 要插入的子节点.prependTo(父节点)
   + 外部插入(兄弟关系的插入)
    5. insertBefore() `在已知节点的前面一个`
    - => 要插入的节点.insertBefore(已知节点)
    6. before() `在已知节点的前面一个`
    - => 已知节点.before(要插入的节点)
    7. insertAfter() `在已知节点的后面一个`
    - => 要插入的节点.insertAfter(已知节点)
    8. after() `在已知节点的后面一个`
    - => 已知节点.after(要插入的节点)

### 删除节点
   + remove()
    - 语法: 元素集合.remove()
    - 作用: 把元素直接移出其父节点
   + empty()
    - 语法: 元素集合.empty()
    - 作用: 把自己变成一个空标签

### 替换节点
   + replaceWidth()
    - 语法: 被替换节点.repalceWith(替换节点)
    - 作用: 使用替换节点, 把被替换节点换掉
   + replaceAll()
    - 语法: 替换节点.replaceAll(被替换节点)

### 克隆节点
   + clone()
    - 语法: 节点.clone()
   + 注意: 当第一个参数为 false 的时候, 第二个参数没有意义
   + 第一个参数
    - 默认是 false, 表示不克隆自己的事件 选填是 true, 表示克隆自己的事件
   + 第二个参数
    - 默认是跟随第一个, 表示是否克隆后代元素的事件
    - > true true  可以, 表示 自己和后代元素事件都克隆
    - > true false 可以, 表示 自己的事件克隆, 后代的事件不克隆
    - > false false可以, 表示 自己和后代元素事件都不克隆
    - > false true 不可以, 表示 自己和后代元素事件都不克隆
    - empty() //把自己变成空标签

### 元素偏移量
   1. offset() `可读写的`
   + 读:
    - => 元素集合.offset()
    - => 返回值: 一个对象数据类型, 里面有左边 和上边的 偏移量
    - => 相对于页面文档流的左上角
   + 写:
    - => 元素集合.offset({ left: xxx, top: xxx })
    - => 绝对设置, 不管你在哪, 不管你是什么方式进行的偏移
    - -> 一定给你移动到距离页面左上角的指定位置

   2. position() `只读的`
    - 没有结构父级的定位 拿到的就不是自己的 而是结构父级的 
    - 要保证结构父级就是定位父级
    - => 元素结合.position()
    - => 返回值: 一个对象数据类型, 里面有这个元素的定位设置的值(left, top)
    - => 但是如果你设置的是 right 和 bottom, 会自动计算 left 和 top 值给你

### 运动函数
**标准运动函数**
   + show()
   + hide()
   + toggle()
    - => 语法: 元素集合.show(时间,运动曲线,运动结束的函数)
**折叠动画**
   + slideDown()
   + slideUp()
   + slideToggle()
    - => 语法: 元素集合.slideDown(时间,运动曲线,运动结束的函数)
**渐隐渐显动画**
   + fadeIn()
   + fadeOut()
   + fadeToggle()
    - => 语法: 元素集合.fadeIn(时间,运动曲线,运动结束的函数)
   + fadeTo()
    - => 语法: 元素集合.fadeTo(时间,指定透明度,运动曲线,运动结束的函数)
**综合动画函数**
   + animate()
    - => 语法: 元素集合.animate({ 要运动的属性 }, 时间, 运动曲线, 运动结束函数)
    - => 注意: 运动的属性 颜色不能动 transform 不能动
**停止动画**
   + stop() `直接停止`
    - 语法: 元素集合.stop()
   + finish() `直接到完成状态`
    - 语法: 元素集合.finish()

