# Typlog Disqus

使用 Typlog 提供的 Disqus 代理服务。服务器费用 $10/年，暂不接受访问量很大的博客。

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

如果遇到 bug 或者问题，请发邮件到 <hi@typlog.com>。
