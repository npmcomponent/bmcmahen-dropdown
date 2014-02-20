*This repository is a mirror of the [component](http://component.io) module [bmcmahen/dropdown](http://github.com/bmcmahen/dropdown). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/bmcmahen-dropdown`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# dropdown

  A simple dropdown menu built using components. 


## Installation

  Using [Component](https://github.com/component/component):

    $ component install bmcmahen/dropdown

  Or use the standalone build located in the `standalone` folder.


## Use
	
  You can enable the html API, which is similar to Bootstrap and accessed through `data` attributes, by calling `listen`.

```javascript
require('dropdown').listen();
```

```html
<a id='dlabel' href='#' data-dropdown-id='mydropdown'>User Menu</a>
<div id='mydropdown' role='menu' aria-labelledby='dlabel' aria-hidden='true' class='Dropdown'>
  <div class='arrow'></div>
  <ul>
    <li><a role='menuitem' tabindex='-1' href='#'> User Settings... </a></li>
    <li><a role='menuitem' tabindex='-1' href='#'> Logout</a></li>
  </ul>
</div>
```


  
  You are encouraged to use `role`, `aria-labelledby` and `aria-hidden` attributes to ensure full accessibility. 

  You can also use the javascript API. 

```javascript
var Dropdown = require('dropdown');
var mine = new Dropdown(anchor, menu);
mine.show();

setTimeout(function(){
  mine.hide();
}, 5000);

mine.on('hide', function(){
  console.log('dropdown is hidden!');
});
```

## License

  MIT
