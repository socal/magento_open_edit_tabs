# magento_open_edit_tabs
Opening magento products in separate tabs to edit.

I had to make a quick hack for magento

Usaeage: 

put snippet in your magento_root/app/design/adminhtml/default/default/temaplte/catalog/product.phtml

```html

<button id="openEditTabs" title="Open Edit Tabs" type="button" class="scalable add" onclick="openEditTabs()" style=""><span><span><span>Open Edit Tabs</span></span></span>
</button>
<script type="text/javascript">
  function openEditTabs() {
    jQuery('a').each(function(key,value){
      if (jQuery(this).html() == 'Edit') {
      	window.open(jQuery(this).attr('href'),"_blank");
      }
    });
  }
</script>

```
