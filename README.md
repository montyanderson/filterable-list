# filterable-list

Table-like data structure stored in Redis.

## Usage

``` javascript
const Redis = require('ioredis');
const FilterableList = require('filterable-list');

const redis = new Redis();

const users = new FilterableList({
	redis,
	name: 'users',
	filters: [
		'name',
		'age'
	],
	length: 10000
});
```
