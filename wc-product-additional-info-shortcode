<?php
/*
 * Plugin Name: Show product atributes table
 * Plugin URL: https://github.com/lomars/product-additional-information-shortcode
 * Description: [product_attributes_table] shortcode
 * Version: 1.0.0
 * Author: Loïc de Marcé (LoicTheAztec in Stack Overflow)
*/

/**
 * Check if WooCommerce is active
 */
if ( in_array( 'woocommerce/woocommerce.php', apply_filters( 'active_plugins', get_option( 'active_plugins' ) ) ) ) {

	if ( ! function_exists( 'display_product_additional_information' ) ) {

		function display_product_additional_information($atts) {

		    // Shortcode attribute (or argument)
		    $atts = shortcode_atts( array(
		        'id'    => ''
		    ), $atts, 'product_additional_information' );

		    // If the "id" argument is not defined, we try to get the post Id
		    if ( ! ( ! empty($atts['id']) && $atts['id'] > 0 ) ) {
		       $atts['id'] = get_the_id();
		    }

		    // We check that the "id" argument is a product id
		    if ( get_post_type($atts['id']) === 'product' ) {
		        $product = wc_get_product($atts['id']);
		    }
		    // If not we exit
		    else {
		        return;
		    }

		    ob_start(); // Start buffering

		    do_action( 'woocommerce_product_additional_information', $product );

		    return ob_get_clean(); // Return the buffered outpout
		}

		add_shortcode('product_additional_information', 'display_product_additional_information');
	}
}
