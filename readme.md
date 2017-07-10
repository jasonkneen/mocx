# MOCX

## Why?

When building apps with Titanium Alloy, it's handy to be able to mock up screens before wiring up to a backend and when doing that it's useful to be able to populate screens with "real" data. But, if you don't have an API ready then what do you do? Mocx is designed to allow you to create create mock collections and modules that are compatible with Alloy's Backbone data-binding.

## Using Movc

You can use Mocx to create a collection and populate a Table or Listview, or create Models on the fly, and it'll support the .fetch() method to pretend to get the model / collection. So you could use it to mock data and even persist data to local storage.

The main things I wanted to achieve were:-

* Easy to add, lightweight library
* Allow easy creation of Models and Collections
* Work with .fetch() instead of .trigger() when getting data
* Extendable

## Quick Start

* [Install from NPM the latest version](https://www.npmjs.com/package/mocx)
or
* [Download the latest version](https://github.com/jasonkneen/mocx) and place in your project (lib folder for Alloy).

```javascript
var mocx = require("mocx");

mocx.createCollection("contacts", [{name : "John Smith"}, {name : "Jane Doe"}]);

```

Once done you can specify a dataCollection on a bindable view and then in the view's controller do:

```javascript
Alloy.Collections.contacts.fetch();
```

More examples / readme updates coming.

## License

<pre>
Copyright Jason Kneen

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
</pre>
