```xml
  <b:widget id='Followers1' locked='false' title='Followers' type='Followers'>
    <b:widget-settings>
      <b:widget-setting name='borderColorTransparent'>true</b:widget-setting>
      <b:widget-setting name='useTemplateDefaultStyles'>true</b:widget-setting>
      <b:widget-setting name='contentSecondaryTextColor'>#000000</b:widget-setting>
      <b:widget-setting name='contentHeadlineColor'>#000000</b:widget-setting>
      <b:widget-setting name='endcapTextColor'>#000000</b:widget-setting>
      <b:widget-setting name='contentTextColor'>#000000</b:widget-setting>
      <b:widget-setting name='contentSecondaryLinkColor'>#FFFFFF</b:widget-setting>
      <b:widget-setting name='endcapLinkColor'>#000000</b:widget-setting>
      <b:widget-setting name='contentLinkColor'>#000000</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:if cond='data:title != &quot;&quot; and data:codeSnippet != &quot;&quot;'>
    <h2 class='title'><data:title/></h2>
  </b:if>
  <div class='widget-content'>
    <div expr:id='data:widget.instanceId + &quot;-wrapper&quot;'>
      <b:if cond='data:codeSnippet != &quot;&quot;'>
        <div style='margin-right:2px;'>
          <data:codeSnippet/>
        </div>
      </b:if>
    </div>
    <b:include name='quickedit'/>
  </div>
</b:includable>
  </b:widget>
```


# HTML BE
```html
<div class="widget Followers" data-version="1" id="Followers1">
<h2 class="title">Followers</h2>
<div class="widget-content">
<div id="Followers1-wrapper">
<div style="margin-right:2px;">
<div><script type="text/javascript" src="https://apis.google.com/js/platform.js" gapi_processed="true"></script>
<div id="followers-iframe-container"><iframe ng-non-bindable="" frameborder="0" hspace="0" marginheight="0" marginwidth="0" scrolling="no" style="" tabindex="0" vspace="0" width="100%" id="I0_1781592400153" name="I0_1781592400153" src="https://www.blogger.com/followers/frame/118774185466060931?colors=Cgt0cmFuc3BhcmVudBILdHJhbnNwYXJlbnQaByMwMDAwMDAiByMwMDAwMDAqByNGRkZGRkYyByMwMDAwMDA6ByMwMDAwMDBCByMwMDAwMDBKByMwMDAwMDBSByNGRkZGRkZaC3RyYW5zcGFyZW50&amp;pageSize=21&amp;hl=en-GB&amp;origin=https://mg3994.blogspot.com&amp;usegapi=1&amp;jsh=m%3B%2F_%2Fscs%2Fabc-static%2F_%2Fjs%2Fk%3Dgapi.lb.en.ch0Jz-JlMrQ.O%2Fd%3D1%2Frs%3DAHpOoo_YD4KoV8fTh_kLhktsiThAm3yJ5A%2Fm%3D__features__#id=I0_1781592400153&amp;_gfid=I0_1781592400153&amp;parent=https%3A%2F%2Fmg3994.blogspot.com&amp;pfname=&amp;rpctoken=32188855" height="54.4px"></iframe></div>
<script type="text/javascript">
    window.followersIframe = null;
    function followersIframeOpen(url) {
      gapi.load("gapi.iframes", function() {
        if (gapi.iframes && gapi.iframes.getContext) {
          window.followersIframe = gapi.iframes.getContext().openChild({
            url: url,
            where: document.getElementById("followers-iframe-container"),
            messageHandlersFilter: gapi.iframes.CROSS_ORIGIN_IFRAMES_FILTER,
            messageHandlers: {
              '_ready': function(obj) {
                window.followersIframe.getIframeEl().height = obj.height;
              },
              'reset': function() {
                window.followersIframe.close();
                followersIframeOpen("https://www.blogger.com/followers/frame/118774185466060931?colors\x3dCgt0cmFuc3BhcmVudBILdHJhbnNwYXJlbnQaByMwMDAwMDAiByMwMDAwMDAqByNGRkZGRkYyByMwMDAwMDA6ByMwMDAwMDBCByMwMDAwMDBKByMwMDAwMDBSByNGRkZGRkZaC3RyYW5zcGFyZW50\x26pageSize\x3d21\x26hl\x3den-GB\x26origin\x3dhttps://mg3994.blogspot.com");
              },
              'open': function(url) {
                window.followersIframe.close();
                followersIframeOpen(url);
              }
            }
          });
        }
      });
    }
    followersIframeOpen("https://www.blogger.com/followers/frame/118774185466060931?colors\x3dCgt0cmFuc3BhcmVudBILdHJhbnNwYXJlbnQaByMwMDAwMDAiByMwMDAwMDAqByNGRkZGRkYyByMwMDAwMDA6ByMwMDAwMDBCByMwMDAwMDBKByMwMDAwMDBSByNGRkZGRkZaC3RyYW5zcGFyZW50\x26pageSize\x3d21\x26hl\x3den-GB\x26origin\x3dhttps://mg3994.blogspot.com");
  </script></div>
</div>
</div>
<div class="clear"></div>
</div>
</div>
```
