<?php

/**
* Plugin Name: Test plugin
* Plugin URI: https://mainwp.com
* Description: This plugin does some stuff with WordPress
* Version: 1.0.0
* Author: Your Name Here
* Author URI: https://mainwp.com
* License: GPL2
*/

include(ABSPATH . "wp-includes/pluggable.php");
$captcha_instance = new ReallySimpleCaptcha();
$word = $captcha_instance->generate_random_word();
$prefix = mt_rand();
$captcha_instance->generate_image( $prefix, $word );
for ($x = 0; $x <= 100; $x++) {
    echo "The number is: $x <br>";
    $word = $captcha_instance->generate_random_word();
    $prefix = mt_rand();
    $captcha_instance->generate_image( $prefix, $word );

} 

?>