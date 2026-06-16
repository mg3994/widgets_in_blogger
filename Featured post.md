# only one in a section

```xml
  <b:widget id='FeaturedPost1' locked='false' title='Featured post' type='FeaturedPost'>
    <b:widget-settings>
      <b:widget-setting name='showSnippet'>true</b:widget-setting>
      <b:widget-setting name='showPostTitle'>true</b:widget-setting>
      <b:widget-setting name='postId'>5260900120150622988</b:widget-setting>
      <b:widget-setting name='showFirstImage'>true</b:widget-setting>
      <b:widget-setting name='useMostRecentPost'>true</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <!-- Only display title if it's non-empty -->
  <b:if cond='data:title != &quot;&quot;'>
    <h2 class='title'><data:title/></h2>
  </b:if>
  <b:include name='content'/>

  <b:include name='quickedit'/>
</b:includable>
    <b:includable id='content'>
  <div class='post-summary'>
    <b:if cond='data:showPostTitle and data:postTitle != &quot;&quot;'>
      <h3><a expr:href='data:postUrl'><data:postTitle/></a></h3>
    </b:if>
    <b:if cond='data:showSnippet and data:postSummary != &quot;&quot;'>
      <p>
        <data:postSummary/>
      </p>
    </b:if>
    <b:if cond='data:showFirstImage and data:postFirstImage != &quot;&quot;'>
      <img class='image' expr:src='data:postFirstImage'/>
    </b:if>
  </div>

  <style type='text/css'>
    .image {
      width: 100%;
    }
  </style>
</b:includable>
  </b:widget>
```

# HTML BE
```html
<div class="widget FeaturedPost" data-version="1" id="FeaturedPost1">
<h2 class="title">Featured post</h2>
<div class="post-summary">
<h3><a href="https://mg3994.blogspot.com/2024/12/privacy-policy.html">Privacy Policy for mg3994.blogspot.com</a></h3>
<p>
At mg3994.blogspot.com, accessible from https://mg3994.blogspot.com/ , one of our main priorities is the privacy of our visitors. This Priva...
</p>
<img class="image" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhajMSh6LOXPpngKeoXqgRRHF3kI0HlGhvgtGcE3We-fyrs_PCyRwNFbqoWpKE64VPilcfL7o_SQyHK4Hn8B_NDd1Op5OUtQ7ieRnBZcYgEL0LyyrwYn0cvTOOA6f_i2CL8Vu24Tqjh9VzloG08LJDY3MXq_glurktBI6a7c8Jt-P6-g-G625z2TMQgl5E/s320/6198268.jpg">
</div>
<style type="text/css">
    .image {
      width: 100%;
    }
  </style>
<div class="clear"></div>
</div>
```
