angu-fixed-header-table-e7
=======================

An AngularJS fixed header scrollable table directive

This is a fork of @cornflourblue angu-fixed-header-table git repo and it includes updates submitted by @Dorian-Fusco and @brandonbird.
The updates are comprised of:
- Less promiscuous selectors.
- Perform calculations on hidden clone rather than original element to prevent FOUCs.
- Perform transformTable when the number of rows of the tbody change to accommodate scrollbar disappearing/reappearing with live data. Updated demo with example.
- Perform transformTable on throttled window resize so that the table columns aren't stuck at a maximum of their originally calculated size.
- Increased scrollBarWidth trim to -4px. Testing the demo in several browsers/platforms seemed to indicate this was better than -2px.
- Fix for IE9 tr height inheritance so that even though the directive fails it at least falls back to a normal looking table.

###Installation

Install using bower: `bower install angu-fixed-header-table-e7`

Alternatively download the code and include the angu-fixed-header-table.js file in your page.

Add the 'anguFixedHeaderTable' directive as a dependency of your AngularJS application:

```javascript
angular.module('myApp', ['anguFixedHeaderTable']);
```

###Usage

Simply add the *fixed-header* attribute to any tables you'd like to have a fixed header:

```html
<table fixed-header>
...
</table>
```

The table height can be set using CSS on the table element or by adding a *table-height* attribute to the table element eg: table-height="500px".
