jQuery UI TinyTable
===========================================================================

Light weight and fully themeable jQuery UI Plugin to generate tables on the
fly with fixed columns, header and/or footer.  Simple usage and a very small
with basic functions like append, prepend or remove one row to the table.  

__More informations and demos:__
Please visit the project page [www.michaelkeck.de](http://michaelkeck.de/projects/jquery/tinytbl/).


API description
---------------------------------------------------------------------------

### Create

Convert a normal table into a TinyTable, simple use this command:  
`$('.selector').tinytbl(object options);`


#### You can use follow options:

- `direction (string 'ltr' | 'rtl')`  
  This option set the text-direction. Default is 'ltr'.  

- `thead (bool true | false)`  
  If your table has a thead and tbody, you can set with this option thead 
  as fixed. Default is true. Notice: If your table has not a thead or 
  tbody this option is always set to false.  

- `tfoot (bool true | false)`  
  If your table has a tfoot and tbody, you can set with this option tfoot 
  as fixed. Default is true. Notice: If your table has not a tfoot or 
  tbody this option is always set to false.  

- `cols (integer 0)`  
  Makes the first columns (counted from ltr or rtl, see also direction) 
  fixed. Default is 0, no columns are fixed. 

- `width (mixed 'auto')`  
  Set the width of TinyTable. You can use values with px, pt, em or %. 
  If you use only a numeric value,  the width is calculated in pixels. 
  When setting this option to a percentage (%) value or to 'auto' the 
  width of TinyTable is calculated to its parent element or $('body').  
  __NEW:__ You can set this parameter to 'cols:X', where X means number of 
  columns (counted from ltr or rtl,  see also direction). Default is  
  'auto' and is equivalent with '100%'.  

- `height (mixed 'auto')`  
  Set the height of TinyTable. You can use values with px, pt, em or %. 
  If you use only a numeric value, the height is calculated in pixels. 
  When setting this option to a percentage (%) value or to 'auto' the 
  height of TinyTable is calculated to its parent element or $('body'). 
  Default is 'auto' and is equivalent with '100%'.  

- `theadcss (string 'ui-widget-header')`  
  Set an user defined CSS class to the fixed table header. Default is 
  'ui-widget-header'.  

- `tbodycss (string 'ui-widget-content')`  
  Set an user defined CSS class to the scrollable area. Default is 
  'ui-widget-content'.  

- `tfootcss (string 'ui-widget-header')`  
  Set an user defined CSS class to the fixed table footer. Default 
  is 'ui-widget-header'.  

- `focus (bool true | false)`  
  Set the focus after TinyTable was created to the scrollable area. 
  Default is false.  

- `renderer (bool true | false)`  
  To support creating of TinyTables on hidden elements (like ui-tabs) 
  with the correct dimensions. But __please note__: This may slow down 
  your site. It's better to create all TinyTables and than to call 
  function like UI-Tabs. Default is false.  


### Destroy

`$('.selector').tinytbl('destroy');`  
Removes the TinyTable and restores the original table.  


### Focus

`$('.selector').tinytbl('focus');`  
Set the focus to the scrollable area.  


### Append a row

`$('.selector').tinytbl('append', object tr-element);`  
Add a new row to TinyTable to the bottom of the body section.  


### Prepend a row

`$('.selector').tinytbl('prepend', object tr-element);`  
Add a new row to TinyTable to the top of the body section.  


### Remove a row

`$('.selector').tinytbl('remove', object tr-element);`  
Removes a specified row from the body section.  



Changelog
---------------------------------------------------------------------------

### Version 2.1.1, released 2012-09-17
__3rd official release__  
- Re-Factor:  
  for supporting WebKit browsers (like Google Chrome and Apple Safari).  
  Ready for jQuery 1.8.1 and jQuery UI 1.8.23.  
- New:  
  Option 'renderer', to support creating of TinyTables on hidden elements (like ui-tabs) with the correct dimensions.  
- Bugfix:  
  Broken layout in WebKit browsers.  

### Version 1.9.1, released 2011-11-10
__2nd official release__  
- New:  
  Calculating the width of TinyTable with the first given columns. If you set as option e.g. width:'cols:2', the first two columns are used to get the width of the TinyTable.  
- Bugfix:  
  Wrong typo for 'paddingRight', now the width should be calculated correctly.  

### Version 1.9.0a, released 2011-10-08
__1st official release__  

Notes
---------------------------------------------------------------------------

### Minimum requirements:
- jQuery 1.6.2  
- jQuery UI Core 1.8.16  
- jQuery UI Widget 1.8.16  

### Tested browsers:
- Firefox (> 11)  
- Google Chrome (> 21)  
- Internet Explorer (> 7)  
- Safari (> 5)  

### Mics:
- To enable fixed table header the table must have a tbody and a thead.  
- To enable fixed table footer the table must have a tbody and a tfoot.  
- Sometimes the table is crashed:  
  Please change in file jquery.ui.tinytbl.css the margins and or remove some 
  borders.  The CSS-file jquery.ui.tinytbl.css only includes correct border 
  colors for the theme UI-Lightness. Please change the lines #15 and #16.  

  
  
