To add Disqus comments to the blog, create new Disqus account and copy script 
generated by Disqus in your theme where you want comments to appear. Usually
right after post content, for example in standard theme:

```html
<div class="post-content">
  @Html.Raw(Model.Content)
</div>

<div id="disqus_thread"></div>
<script>
  (function () {  // DON'T EDIT BELOW THIS LINE
    var d = document, s = d.createElement('script');
    s.src = '//yoursite.disqus.com/embed.js';
    s.setAttribute('data-timestamp', +new Date());
    (d.head || d.body).appendChild(s);
  })();
</script>
```