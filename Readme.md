# Typlog Disqus

使用 Typlog 提供的 Disqus 代理服务。服务器费用 $10/年，暂不接受访问量很大的博客。

## 使用方法

注册：<https://typlog.com/account/signup/disqus>

注册后，在博客文章页面插入如下代码：

```html
<div id="disqus_thread"></div>
<script>
  disqus_shortname = 'your-disqus-shortname';
  disqus_page_url = 'http://your-blog-post-url';  // optional
  disqus_page_title = 'your blog post title';  // optional
</script>
<script src="//a.typcdn.com/embed/disqus.js"></script>
```

上面的 `disqus.js` 会先试着加载 Disqus，如果不成功，则会加载 Typlog 的代理。

注意事项：

1. 你需要在 Disqus 的设置里打开 Allow guests to comment
2. 由于 "Pre-moderation is always enabled for guest comments"，匿名用户的评论你需要在 Disqus Admin 里审核

## 显示评论数

Typlog Disqus 会自动显示文章页面的 Comment Count，你不需要在文章页面里加载 `count.js`。

如果要在首页加载评论数的话，推荐使用异步的方式加载`count.js`，Typlog 的这个代理不提供此功能：

```html
<script>
var el = document.createElement('script');
el.id = 'dsq-count-scr';
el.src = 'https://' + disqus_shortname + '.disqus.com/count.js';
el.async = true;
document.body.appendChild(el);
</script>
```

## 联系

如果遇到 bug 或者问题，请发邮件到 <hi@typlog.com>。
