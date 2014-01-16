Easy TinyMCE Class
==================

An Helper Class to create TinyMCE button and Shortcode editor

##Installation

1. Download the pack from here and place it in your plugin or theme.
2. Include `Easy-tinyMCE.class.php` and `Easy-tinyMCE-content.class.php` in your theme's functions.php file or plugin file
3. Now call the class just like the code below.

<pre>
$shortwell_TinyMCE = new Easy_TinyMCE_Class;
$shortwell_TinyMCE->title = 'Shortcode Tittle';
$shortwell_TinyMCE->js_url = get_template_directory_uri().'/tinymce/tinyMCE-plugin.js';
$shortwell_TinyMCE->uid = 'shortcode_unique_id';
$shortwell_TinyMCE->templates = array(
	array('name'=> 'Soundcloud', 'url'=> get_template_directory().'/tinymce/audio-TinyMCE.php'),
	array('name'=> 'Alert', 'url'=> get_template_directory().'tinymce/alert-TinyMCE.php'),	
	array('name'=> 'Accordion', 'url'=> get_template_directory().'tinymce/accordion-TinyMCE.php'),	
);
</pre>

4. Now find the `tinyMCE-plugin-sample.js` and rename it to `tinyMCE-plugin.js` and open it
5. Replace the `_____id_____` with the `shortcode_unique_id` , `_____title_____` with shortcode title and `____icon_____` with icon path
6. create and new file call `audio-TinyMCE.php` and put the code like below
<pre>
<?php
$tinyMCE = new Easy_TinyMCE_Class_content;
$tinyMCE->id = 'accordion';
$tinyMCE->shortcode = 'accordion';
$tinyMCE->content = true;
$tinyMCE->options = array(
	array(
		'id' => 'class',
		'field' => 'text', //text, textarea, select post-select, tax-select
		'title' => __( 'Div Class', 'shortwell_textdomain' ),
		'des' => '',
		'post_type' => '',
		'multiple' => false,
		'content' => false,
		'option' => '',
	),
	
	array(
		'id' => 'link',
		'field' => 'textarea', //text, textarea, select post-select, tax-select
		'title' => __( 'Link', 'shortwell_textdomain' ),
		'des' => '',
		'post_type' => '',
		'std' => '[accordion_item title="Accordion 1"] .... Content onw11 ....[/]
		[accordion_item title="Accordion 1"] .... Content onw11 ....[/accordion_item]
		[accordion_item title="Accordion 1"] .... Content onw11 ....[/accordion_item]',
		'multiple' => false,
		'content' => true,
		'option' => '',
	)
	
);
$tinyMCE->html();
</pre>

That's all

I have included an example folder with the working example. Don't forget to check it
