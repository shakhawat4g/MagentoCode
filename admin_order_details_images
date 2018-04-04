File Path: app/design/adminhtml/default/default/template/sales/order/view/items/renderer/default.phtml



<?php $product = Mage::getModel('catalog/product')->setStoreId($_item->getOrder()->getStoreId())->load($_item->getProductId());?>
<?php $_pullProduct = Mage::getModel('catalog/product')->load($_item->getProductId()); ?>
<?php
try{
  $image = Mage::helper('catalog/image')->init($product, 'small_image')->resize(75);
}
catch(Exception $e) {
  $image = Mage::getDesign()->getSkinUrl('images/catalog/product/placeholder/image.jpg',array('_area'=>'frontend'));  
}

 //$image = Mage::helper('catalog/image')->init($product, 'small_image')->resize(75);
?>
<?php if ($image) : ?>
<p align="center">
  <a target="_blank" rel="external" href="<?php echo Mage::getUrl() . $_pullProduct->getData('url_path'); ?>"><img src="<?php echo $image;  ?>" width="75" height="75" /></a>
</p>
<?php endif; ?>
