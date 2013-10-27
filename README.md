jquery-gpopover
===============

A simple jQuery plugin for creating popover elements similar to Google's new 'apps' launcher/switcher.

## Usage

Create a trigger element on your page (for example, a link or a button), and set the `data-popover` attribute to the ID of the element you wish to pop over.

    <button id="my-trigger" data-popover="my-popover">Click Me</button>
    
Create the popover content element somewhere in your document. You may place this wherever you wish in the document (for example, at the end or after your trigger element). Simply make sure the ID matches that which your trigger has, and give it the class of `gpopover` to make sure it is styled correctly and hidden initially.

    <div id="my-popover" class="gpopover">
        This is where your popover content goes.
    </div>
    
Initialise the plugin on your trigger element. That's it.

    $('#my-trigger').gpopover();

You can also trigger a show or hide through code (i.e. without the user clicking), by invoking the show or hide methods.:

    $('#my-trigger').gpopover('show');
    $('#my-trigger').gpopover('hide');

This is normally best done after initialising your popovers as above, but if it hasn't been done, it will do so using default options before then acting.
    
## Demo

Want to see what the popovers look like? Check out the [simple example](http://markembling.github.io/jquery-gpopover/).

## Customising the Plugin

### Options

The plugin has a few options which can be passed to it:

<table>
    <tr>
        <th>Property</th>
        <th>Default</th>
        <th>Description</th>
    </tr>
    
    <tr>
        <td><code>width</code></td>
        <td>250</td>
        <td>The width of the popover element (pixels)</td>
    </tr>
    <tr>
        <td><code>fadeInDuration</code></td>
        <td>65</td>
        <td>Duration of popover fade-in animation (ms)</td>
    </tr>
    <tr>
        <td><code>fadeOutDuration</code></td>
        <td>65</td>
        <td>Duration of popover fade-out animation (ms)</td>
    </tr>
    <tr>
        <td><code>viewportSideMargin</code></td>
        <td>10</td>
        <td>Space to leave at the side, if up against the viewport edge (pixels)</td>
    </tr>
    <tr>
        <td><code>preventHide</code></td>
        <td>false</td>
        <td>Prevent hiding when clicking within popover (true/false)</td>
    </tr>
    <tr>
        <td><code>onShow</code></td>
        <td>(none)</td>
        <td>Callback to be run when the popover is shown. <code>this</code> 
            is the trigger element and the first argument passed to the 
            function is the popover element (both jQuery-wrapped).</td>
    </tr>
    <tr>
        <td><code>onHide</code></td>
        <td>(none)</td>
        <td>Callback to be run when the popover is hidden. Same as  <code>onShow</code>.</td>
    </tr>
</table>

### Styling

The default styling is visually similar to Google's pop-out apps menu on their recent redesign, as I like the clean lines and look. However, the appearance can be modified by changing the styles in the `jquery.gpopover.css` stylesheet.

The main popover element has the `gpopover` class, and the arrow is made up of two elements with the classes `gpopover-arrow` and `gpopover-arrow-shadow`. The latter is positioned 1 pixel higher to give the shadow/outline effect.

## License

Licensed under the BSD (3 clause) license.  
Copyright (c) 2013 Mark Embling (markembling.info).
