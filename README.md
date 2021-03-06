# evo-css-switch
A nifty little UI toggle theme switcher that toggles between two CSS style sheet links.

[Demo](https://labelle.github.io/evo-css-switch/).

For a bootstrap toggle version, check out [Bootstrap CSS Switch](https://github.com/labelle/bootstrap-css-switch).

For a pulldown menu CSS theme switcher, check out [Evo CSS Pulldown] (https://github.com/labelle/evo-css-pulldown).

## documentation

In addition to this README file, you'll find helpful 'comments' sprinkled throughout the HTML, CSS, and JavaScript files.

## contribution

If you find any glitches or have ideas for improvements, please submit a Github issue or pull request.

## usage

You will need the following code snippets in your your HTML documents.

CSS links, for the document head.

```html
<!-- Place css here with unique title like "style1,style2,style3....." and with class="new" to toggle through all styles -->
<link rel="stylesheet" type="text/css" href="white.css" title="style1" class="new" media="screen" />
<link rel="stylesheet" type="text/css" href="black.css" title="style2" class="new" media="screen" />
<!-- This style sheet is for toggle buttom -->
<link rel="stylesheet" href="view.css">
```

If you want to add more styles to the switch, append this CSS style sheet.

```html
<link rel="stylesheet" type="text/css" href="<styleheet path>" title="style1" class="new" media="screen" />
```

HTML markup, for the document body.

```html
<!-- toggle button start -->
<div class="pspec-checkbox-container" id="pspec-toggle-outlines-container">
        <input type="checkbox" id="pspec-toggle-outlines" name="pspec-toggle-outlines" class="pspec-toggle round-corners input-text" checked="">
      <label id="pspec-specs-toggle" class="pspec-toggle-label pspec-switch pspec-switch--green" for="pspec-toggle-outlines"></label>
 </div>
 <!-- toggle button End -->
 
<h1 id='toggler'>Here is text.</h1>
```

Scripts, at the bottom of the document body.

```html

<!-- link to external scripts here if needed -->
<script src="jquery.js"></script>
    <!-- Include all compiled plugins (below), or include individual files as needed -->
	
<!-- link to toggle scripts -->	
	<script src="stylesheetToggle.js"></script>
        <script>
$.stylesheetInit();
   
// This code loops through the stylesheets when you click the link with
// an ID of "toggler" below.
$("#pspec-toggle-outlines").bind(
 "click",
 function(e)
 {
  $.stylesheetToggle("slow");
 }
);
        </script>
```

## dependencies

In your project, link to the following files.

* jquery.js
* stylesheetToggle.js
* view.css

Replace these sample CSS files with your own CSS.

* white.css
* black.css


