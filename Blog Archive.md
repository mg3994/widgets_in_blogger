```xml
<b:widget id='BlogArchive1' locked='false' title='Blog Archive' type='BlogArchive'>
    <b:widget-settings>
      <b:widget-setting name='showStyle'>HIERARCHY</b:widget-setting>
      <b:widget-setting name='yearPattern'>yyyy</b:widget-setting>
      <b:widget-setting name='showWeekEnd'>true</b:widget-setting>
      <b:widget-setting name='monthPattern'>MMMM</b:widget-setting>
      <b:widget-setting name='dayPattern'>MMM dd</b:widget-setting>
      <b:widget-setting name='weekPattern'>MM/dd</b:widget-setting>
      <b:widget-setting name='chronological'>true</b:widget-setting>
      <b:widget-setting name='showPosts'>true</b:widget-setting>
      <b:widget-setting name='frequency'>MONTHLY</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:if cond='data:title != &quot;&quot;'>
    <h2><data:title/></h2>
  </b:if>
  <div class='widget-content'>
  <div id='ArchiveList'>
  <div expr:id='data:widget.instanceId + &quot;_ArchiveList&quot;'>
    <b:include cond='data:style == &quot;HIERARCHY&quot;' data='data' name='interval'/>
    <b:include cond='data:style == &quot;FLAT&quot;' data='data' name='flat'/>
    <b:include cond='data:style == &quot;MENU&quot;' data='data' name='menu'/>
  </div>
  </div>
  <b:include name='quickedit'/>
  </div>
</b:includable>
    <b:includable id='flat' var='data'>
  <ul class='flat'>
    <b:loop values='data:data' var='i'>
      <li class='archivedate'>
        <a expr:href='data:i.url'><data:i.name/></a> (<data:i.post-count/>)
      </li>
    </b:loop>
  </ul>
</b:includable>
    <b:includable id='interval' var='intervalData'>
  <b:loop values='data:intervalData' var='interval'>
    <ul class='hierarchy'>
      <li expr:class='&quot;archivedate &quot; + data:interval.expclass'>
        <b:include cond='data:interval.toggleId' data='interval' name='toggle'/>
        <a class='post-count-link' expr:href='data:interval.url'>
          <data:interval.name/>
        </a>
        <span class='post-count' dir='ltr'>(<data:interval.post-count/>)</span>
        <b:include cond='data:interval.data' data='interval.data' name='interval'/>
        <b:include cond='data:interval.posts' data='interval.posts' name='posts'/>
      </li>
    </ul>
  </b:loop>
</b:includable>
    <b:includable id='menu' var='data'>
  <select expr:id='data:widget.instanceId + &quot;_ArchiveMenu&quot;'>
    <option value=''><data:title/></option>
    <b:loop values='data:data' var='i'>
      <option expr:value='data:i.url'><data:i.name/> (<data:i.post-count/>)</option>
    </b:loop>
  </select>
</b:includable>
    <b:includable id='posts' var='posts'>
  <ul class='posts'>
    <b:loop values='data:posts' var='post'>
      <li><a expr:href='data:post.url'><data:post.title/></a></li>
    </b:loop>
  </ul>
</b:includable>
    <b:includable id='toggle' var='interval'>
  <a class='toggle' href='javascript:void(0)'>
    <span expr:class='&quot;zippy&quot; + (data:interval.expclass == &quot;expanded&quot; ? &quot; toggle-open&quot; : &quot;&quot;)'>
      <b:if cond='data:interval.expclass == &quot;expanded&quot;'>
        &#9660;&#160;
      <b:elseif cond='data:blog.languageDirection == &quot;rtl&quot;'/>
        &#9668;&#160;
      <b:else/>
        &#9658;&#160;
      </b:if>
    </span>
  </a>
</b:includable>
  </b:widget>
```

# HTML BE
```html
<div class="widget BlogArchive" data-version="1" id="BlogArchive1">
<h2>Blog Archive</h2>
<div class="widget-content">
<div id="ArchiveList">
<div id="BlogArchive1_ArchiveList">
<ul class="hierarchy">
<li class="archivedate expanded">
<a class="toggle" href="javascript:void(0)">
<span class="zippy toggle-open">

        ▼&nbsp;
      
</span>
</a>
<a class="post-count-link" href="https://mg3994.blogspot.com/2024/">
2024
</a>
<span class="post-count" dir="ltr">(1)</span>
<ul class="hierarchy">
<li class="archivedate expanded">
<a class="toggle" href="javascript:void(0)">
<span class="zippy toggle-open">

        ▼&nbsp;
      
</span>
</a>
<a class="post-count-link" href="https://mg3994.blogspot.com/2024/12/">
December
</a>
<span class="post-count" dir="ltr">(1)</span>
<ul class="posts">
<li><a href="https://mg3994.blogspot.com/2024/12/privacy-policy.html">Privacy Policy for mg3994.blogspot.com</a></li>
</ul>
</li>
</ul>
</li>
</ul>
</div>
</div>
<div class="clear"></div>
</div>
</div>
```
