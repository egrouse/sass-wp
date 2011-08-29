This is a basic plugin for WordPress, which allows you to parse SCSS/SASS files and convert them into CSS files usable by browsers.

More info on SASS: http://sass-lang.com/
Makes use of PHamlP: http://code.google.com/p/phamlp/

USAGE
-----
<h3>Options</h3>
First of all, you need to set the options for the SASS parser. Ideally, you should  do this near the start of your site loading process - before the ```<head>``` tag gets output, anyway:

```$SASS->set_sass_options( $options );```

$options should be an Array containing the desired options for the SASS parser. To view a list of all these options, go here: http://code.google.com/p/phamlp/wiki/SassOptions

<h3>Rendering a file</h3>
You can then render a file. To do so, use the following PHP code. The function returns the (relative) path to the created CSS file, so you can use it in ```enqueue_style()``` or a standard ```<link>``` element. Note that input should also be entered as a relative path - relative to the root of your template directory.

```$css_link = scss_file( 'style.scss', 'sass.css' );
echo $css_link;
/* Outputs: /wp-content/themes/twentyten/sass.css */```

<h3>CSS Comment</h3>
By default, a warning is added to the created CSS file informing the user not to edit it. You can disable it with the following command, <b>before</b> calling ```scss_file()```:

``` $SASS->add_comment( false );```