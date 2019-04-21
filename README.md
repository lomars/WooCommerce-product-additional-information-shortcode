# Product additional information shortcode <br> _(For WooCommerce)_
> **Display additional product information as weight, dimensions and product attributes anywhere.**

The shortcode has an unique optional "id" argument _(the product id)_.
If the "id" argument is not defined, the shortcode will try to get the post ID _(checking that is a product Id)_.

### SHORTCODE USAGE

1. With a defined "id" argument (the product ID):

    `[product_additional_information id='37']`
    
    or in php:
    
    `echo do_shortcode("[product_additional_information id='37']");`
    
2. Without a defined "id" argument _(In an existing product page when **"additional information"** product tab is removed for example)_:

    `[product_additional_information]`
    
    or in php:
    
    `echo do_shortcode("[product_additional_information]");`
    
You will get something like:

![alt text](https://i.stack.imgur.com/sOK3f.png)

Based on my Stack Overflow answer: [WooCommerce product additional information shortcode](https://stackoverflow.com/questions/50225929/woocommerce-product-additional-information-shortcode/50228540#50228540)

Made on Stack Overflow on 2018-05-02 _(Updated on 2019-04-22)_
