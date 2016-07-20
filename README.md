## March 2016 Class Server

### Usage

Root URL - [https://class-server.herokuapp.com/](https://class-server.herokuapp.com/)


1. Start with the __Root URL__ above
2. Add the word `/collections` to the end of it
3. Then add your own _unique_ word after it. 
  - example: `/collections/tim`
  - example: `/collections/tims-todos`
  - example: `/collections/asldfjasdjfpoiwre5858323lasdf`

> Ok, you get the point.

Everything you need to know is that it follows a standard [REST API](http://www.restapitutorial.com/)

For instance:

```js
const url = 'https://class-server.herokuapp.com/collections/tims-whiskey/';

// Note: The following is pseudo code. Feel free to use any ajax library for this.
// Just assume that `http` is some ajax library, you could use jQuery (`$.ajax()`) or angular (`$http`) etc.

// Create - create a new whiskey
let whiskey = { name: 'Blantons', type: 'Bourbon' };
http.post(url, whiskey);

// Read - all the whiskeys
http.get(url);

// Read - a single whiskey
http.get(url + whiskey.id);

// Update - update a value to our whiskey
whiskey.rating = '5 stars';
http.put(url + whiskey.id);

// Delete - remove a whiskey
http.delete(url + whiskey.id);
```


