# Popbox.js
Popbox.js is a tiny javascript plugin for creating stackable modals.
It is fully customizable and dependency free.


[Demo](https://oncebot.github.io/popbox.js/)

![Popbox. animated](https://oncebot.github.io/popbox.js/animated.popbox.js.gif)


### Installation

1. Add the popbox.css file to the head of your html.
2. Add the popbox.js file to the head of your html or right before the closing body tag.
3. Add this code after the popbox.js script tag to initialize the plugin.
```
<script type="text/javascript">
  var popbox = new Popbox({
        blur:true,
        overlay:true,
      });
</script>
	
```

### Example HTML
```
 <div data-popbox-id="mypopbox1" class="popbox">
   <div class="popbox_container">
    Popbox content 1
    <button data-popbox-close="mypopbox1">Close</button>
   </div>
 </div>

 <div data-popbox-id="mypopbox2" class="popbox">
   <div class="popbox_container">
    Popbox content 2
   </div>
    <button data-popbox-close="mypopbox2">Close</button>
 </div>

 <div class="popbox_main_content">
    Main content of the page

    <button data-popbox-target="mypopbox1">
    Open mypopbox 1
    </button>

    <button data-popbox-target="mypopbox2">
    Open mypopbox 2
    </button>
&nbsp </div>
 ```

### Options

blur : set it to true for blur effect on the main content (Default:false)

### API

Open and close popbox with api
```
<script type="text/javascript">
  var popbox =   new Popbox({
        blur:true,
        overlay:true,
      });

  //open a popbox
  popbox.open('mypopbox1');	
  //close a popboxs
  popbox.close('mypopbox1');	
  //close all popboxs
  popbox.clear(); 
</script>
```

### Emitted events 
* 'popbox_opening': when a popbox is opening, that popbox element will emit this event..
* 'popbox_opened': when a popbox is opened, that popbox element will emit this event..
* 'popbox_closing': when a popbox is closing, that popbox element will emit this event..
* 'popbox_closed': when a popbox is closed, that popbox element will emit this event..

[Oncebot](https://oncebot.com)
