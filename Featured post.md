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
