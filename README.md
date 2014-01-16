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

4. Now 
