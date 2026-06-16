```xml
  <b:widget id='BlogSearch1' locked='false' title='Search This Blog' type='BlogSearch'>
    <b:includable id='main'>
    <!-- only display title if it's non-empty -->
    <b:if cond='data:title != &quot;&quot;'>
      <h2 class='title'><data:title/></h2>
    </b:if>

    <div class='widget-content'>
      <div expr:id='data:widget.instanceId + &quot;_form&quot;'>
        <form class='gsc-search-box' expr:action='data:blog.searchUrl'>
          <b:attr cond='not data:view.isPreview' name='target' value='_top'/>
          <table cellpadding='0' cellspacing='0' class='gsc-search-box'>
            <tbody>
              <tr>
                <td class='gsc-input'>
                  <input autocomplete='off' class='gsc-input' expr:value='data:view.isSearch ? data:view.search.query.escaped : &quot;&quot;' name='q' size='10' title='search' type='text'/>
                </td>
                <td class='gsc-search-button'>
                  <input class='gsc-search-button' expr:value='data:messages.search' title='search' type='submit'/>
                </td>
              </tr>
            </tbody>
          </table>
        </form>
      </div>
    </div>

    <b:include name='quickedit'/>
  </b:includable>
  </b:widget>


```

# HTML BE

```html
<div class="widget BlogSearch" data-version="1" id="BlogSearch1">
<h2 class="title">Search This Blog</h2>
<div class="widget-content">
<div id="BlogSearch1_form">
<form action="https://mg3994.blogspot.com/search" class="gsc-search-box" target="_top">
<table cellpadding="0" cellspacing="0" class="gsc-search-box">
<tbody>
<tr>
<td class="gsc-input">
<input autocomplete="off" class="gsc-input" name="q" size="10" title="search" type="text" value="">
</td>
<td class="gsc-search-button">
<input class="gsc-search-button" title="search" type="submit" value="Search">
</td>
</tr>
</tbody>
</table>
</form>
</div>
</div>
<div class="clear"></div>
</div>
```
