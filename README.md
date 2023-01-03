There are various methods to get an input textbox value directly (without wrapping the input element inside a form element):

### Method 1

document.getElementById('textbox_id').value to get the value of desired box

For example
document.getElementById("searchTxt").value;

Note: Method 2,3,4 and 6 returns a collection of elements, so use [whole_number] to get the desired occurrence. For the first element, use [0], for the second one use [1], and so on...

### Method 2

Use document.getElementsByClassName('class_name')[whole_number].value which returns a Live HTMLCollection

For example
document.getElementsByClassName("searchField")[0].value; if this is the first textbox in your page.

### Method 3

Use document.getElementsByTagName('tag_name')[whole_number].value which also returns a live HTMLCollection

For example
document.getElementsByTagName("input")[0].value;, if this is the first textbox in your page.

### Method 4

document.getElementsByName('name')[whole_number].value which also >returns a live NodeList

For example
document.getElementsByName("searchTxt")[0].value; if this is the first textbox with name 'searchtext' in your page.

### Method 5

Use the powerful document.querySelector('selector').value which uses a CSS selector to select the element

#### For example

- document.querySelector('#searchTxt').value; selected by id
- document.querySelector('.searchField').value; selected by class
- document.querySelector('input').value; selected by tagname
- document.querySelector('[name="searchTxt"]').value; selected by name

### Method 6

document.querySelectorAll('selector')[whole_number].value which also uses a CSS selector to select elements, but it returns all elements with that selector as a static Nodelist.

#### For example

- document.querySelectorAll('#searchTxt')[0].value; selected by id
- document.querySelectorAll('.searchField')[0].value; selected by class
- document.querySelectorAll('input')[0].value; selected by tagname
- document.querySelectorAll('[name="searchTxt"]')[0].value; selected by name
