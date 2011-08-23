Lazy Image Loader For Magento
====================================

## INSTALLATION

* 1) Extract zip archive and copy contents to the app/folder of your Magento installation
* 2) Open the file "app/design/frontend/default/default/catalog/product/list.phtml"

search for:
<img src="<?php echo $this->helper('catalog/image')->init($_product, 'small_image')->resize(135); ?>"
width="135" height="135" alt="<?php echo $this->stripTags($this->getImageLabel($_product,      'small_image'), null, true) ?>" />

replace with:
replace with
<img class="lazy" long-desc="<?php echo $this->helper('catalog/image')->init($_product, 'small_image')->resize(135); ?>"
src="<?php echo $this->getSkinUrl('images/lazy_image_loader/loader.gif'); ?>"  alt="<?php echo $this->stripTags($this->getImageLabel($_product, 'small_image'), null, true) ?>" />

* 3) Clear the cache in Admin > System > Cache Management


