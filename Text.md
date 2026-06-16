```xml
  <b:widget id='Text1' locked='false' title='Hi This is a Sample text' type='Text'>
    <b:widget-settings>
      <b:widget-setting name='content'>Nothing her to show</b:widget-setting>
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
