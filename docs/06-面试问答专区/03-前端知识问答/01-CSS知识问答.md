
<!-- -->
## 如何做垂直居中

:::info 相关内容
- [html中div使用CSS实现水平/垂直居中的多种方式](https://zhuanlan.zhihu.com/p/382710261)
:::

- line-height:1
- flex布局
- 绝对定位
- 使用table布局

<!-- -->
## CSS相关问题

:::info 相关内容
- [一文学会CSS基本选择器和复合选择器](https://zhuanlan.zhihu.com/p/141183913)
- [【果冻公开课】第三课：CSS选择器都有哪些类型](https://www.zhihu.com/zvideo/1198694654876827648)
- [css选择器优先级顺序是什么？css基本选择器优先级的介绍](https://zhuanlan.zhihu.com/p/139236640)
:::

### CSS有哪些选择器,选择器的优先级

- 基本选择器
  - ID选择器
  - 标签选择器(也叫元素选择器)
  - 类选择器
  - 伪类选择器(:hover,:active)
  - 属性选择器
  - 通配符选择器
- 复合选择器
  - 父子选择器(跟结构相关)
  - 后代选择器(跟结构相关)
  - 兄弟选择器(跟结构相关)
  - 交集选择器(条件选择器)
  - 并集选择器(也叫组合选择器或群组选择器)

### CSS选择器优先级最高到最低顺序

1. id选择器（#myid）
2. 类选择器（.myclassname）
3. 标签选择器（div,h1,p）
4. 子选择器（ul < li）
5. 后代选择器（li a）
6. 伪类选择（a:hover,li:nth-child）
