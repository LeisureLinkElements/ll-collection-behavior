# ll-collection

Adds collection-management functionality to an element with a repeating template.

## Features:

- **Add item** with optional data
- **Delete item** by index, or when item fires event
- **Trash / un-trash item** when item fires event
- **Toggles HTML class 'lcb-trashed'** on the item's element.
- **Empty trash**

## Usage

1. Add this behavior to an element with a dom-repeat template.
1. Add a 'lcb-items-name' property to the element.
1. Set the value to the name of the property to which the dom-repeat items are bound.
1. Optionally add a delete button to each item by adding it within the dom-repeat template. Example:

        <button on-tap="_lcbDeleteMe">DELETE THIS ITEM</button>
1. Optionally add trash/un-trash button. (The _lcbTrashMe method toggles trashing.) Example:

        <button on-tap="_lcbTrashMe">TRASH / UNTRASH THIS ITEM</button>
1. Empty the trash by calling lcbEmptyTrash().
1. Optionally define the 'lcb-trashed' class in the element's dom module to indicate which items are trashed.

## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install


## Playing With Your Element

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polyserve

And you can run it via:

    polyserve

Once running, you can preview your element at
`http://localhost:8080/components/ll-table/`, where `ll-table` is the name of the directory containing it.

Mess around with /demo/sample-data.js


## Testing Your Element

Simply navigate to the `/test` directory of your element to run its tests. If
you are using Polyserve: `http://localhost:8080/components/ll-table/test/`


### web-component-tester

The tests are compatible with [web-component-tester](https://github.com/Polymer/web-component-tester).
Install it via:

    npm install -g web-component-tester

Then, you can run your tests on _all_ of your local browsers via:

    wct

#### WCT Tips

`wct -l chrome` will only run tests in chrome.

`wct -p` will keep the browsers alive after test runs (refresh to re-run).

`wct test/some-file.html` will test only the files you specify.
