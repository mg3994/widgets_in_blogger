#### only one in a section

```xml
 <b:widget id='Profile1' locked='false' title='About Me' type='Profile'>
    <b:widget-settings>
      <b:widget-setting name='showaboutme'>true</b:widget-setting>
      <b:widget-setting name='showlocation'>true</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
    <b:if cond='data:title != &quot;&quot;'>
      <h2><data:title/></h2>
    </b:if>
    <div class='widget-content'>
    <b:if cond='data:team'> <!-- team blog profile -->
      <ul>
        <b:loop values='data:authors' var='i'>
          <li><a class='profile-name-link g-profile' expr:href='data:i.userUrl' expr:style='&quot;background-image: url(&quot; + data:i.profileLogo + &quot;);&quot;'><data:i.display-name/></a></li>
        </b:loop>
      </ul>

    <b:else/> <!-- normal blog profile -->

      <b:if cond='data:photo.url != &quot;&quot;'>
        <a expr:href='data:userUrl'><img class='profile-img' expr:alt='data:messages.myPhoto' expr:height='data:photo.height' expr:src='data:photo.url' expr:width='data:photo.width'/></a>
      </b:if>

      <dl class='profile-datablock'>
        <dt class='profile-data'>
          <a class='profile-name-link g-profile' expr:href='data:userUrl' expr:style='&quot;background-image: url(&quot; + data:profileLogo + &quot;);&quot;' rel='author'>
            <data:displayname/>
          </a>
        </dt>

        <b:if cond='data:showlocation'>
          <dd class='profile-data'><data:location/></dd>
        </b:if>

        <b:if cond='data:aboutme != &quot;&quot;'><dd class='profile-textblock'><data:aboutme/></dd></b:if>
      </dl>
      <a class='profile-link' expr:href='data:userUrl' rel='author'><data:viewProfileMsg/></a>
    </b:if>

     <b:include name='quickedit'/>
    </div>
  </b:includable>
  </b:widget>
```

# HTML BE 
```html
<div class="widget Profile" data-version="1" id="Profile1">
<h2>About Me</h2>
<div class="widget-content">
<dl class="profile-datablock">
<dt class="profile-data">
<a class="profile-name-link g-profile" href="https://draft.blogger.com/profile/02949392009900018502" rel="author" style="background-image: url(//draft.blogger.com/img/logo-16.png);">
mg3994
</a>
</dt>
<dd class="profile-data">
</dd>
</dl>
<a class="profile-link" href="https://draft.blogger.com/profile/02949392009900018502" rel="author">View my complete profile</a>
<div class="clear"></div>
</div>
</div>
```
