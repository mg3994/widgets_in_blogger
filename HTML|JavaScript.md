```xml
  <b:widget id='HTML1' locked='false' title='This Html/js' type='HTML'>
    <b:widget-settings>
      <b:widget-setting name='content'><![CDATA[<h1>Hello this is html</h1> <script src="" /></script>]]></b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <!-- only display title if it's non-empty -->
  <b:if cond='data:title != &quot;&quot;'>
    <h2 class='title'><data:title/></h2>
  </b:if>
  <div class='widget-content'>
    <data:content/>
  </div>

  <b:include name='quickedit'/>
</b:includable>
  </b:widget>
```
# HTML BE
```html
<div class="widget HTML" data-version="1" id="HTML1">
<h2 class="title">This Html/js</h2>
<div class="widget-content">
<h1>Hello this is html</h1> <script src=""></script>
</div>
<div class="clear"></div>
</div>
```
