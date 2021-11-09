

:::info 相关文章
- [浅谈CSRF攻击方式](https://www.cnblogs.com/hyddd/archive/2009/04/09/1432744.html)
:::

## 完成一次CSRF攻击的步骤

从上图可以看出,要完成一次CSRF攻击,受害者必须依次完成两个步骤:

1. 登录受信任网站A,并在本地生成Cookie.
2. 在不登出A的情况下,访问危险网站B(B网站有静态资源的加载方式).

## 那些方法可以制造CSRF攻击

一切静态资源加载方式都可以
- JSONP方式
- img标签的src
- scripts


## 示例

```html
银行网站A，它以GET请求来完成银行转账的操作，如：http://www.mybank.com/Transfer.php?toBankId=11&money=1000  
危险网站B，它里面有一段HTML的代码如下：

<img src=http://www.mybank.com/Transfer.php?toBankId=11&money=1000/>
```

## 怎样预防
Double Cookie Defense:
将 token 设置在 Cookie 中，在提交（POST、PUT、PATCH、DELETE 等）请求时提交 Cookie，并通过 header 或者 body 带上 Cookie 中的 token，服务端进行对比校验。