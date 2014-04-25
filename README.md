# HTML DOM Parser

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

* **More info**: ITERNOVA [http://www.iternova.net]
* **Based on**: http://sourceforge.net/projects/simplehtmldom


## Example 

```php
Usage Example:
// Create a DOM object
$dom = new HTMLDOMParser\DOM();

// Load HTML from a string
$dom->load('<div id="hello_div" class="foo">Hello World!</div>');

// Find an element
$element = $dom->find( 'div' );

// Modify elements
foreach( $dom->find( '.foo' ) as $element ) {
	$element->innertext = 'Hi World!';
}

// Also... modify first div element style...
$dom->find( 'div', 0 )->style = 'border:1px solid #CCCCCC;';

// Or CSS classes... modify first div element...
$dom->find( 'div[id=hello_div]', 0 )->class = 'bar';

// Or content!
$dom->find( 'div', 0)->innertext = 'Hi again!';

// Return HTML from DOM tree
$str_html = $dom->get_html();

```

## Composer.json
In order to use composer, complete your composer.json file with:
```js
{
    "require": {
       "jorgecasas/htmldomparser": "dev-master"
    }
}
```