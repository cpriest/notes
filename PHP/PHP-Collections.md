# Collections

## Extending Collections

Collections are "macroable", which allows you to add additional methods to the Collection class at run time. For example, the following code adds a toUpper method to the Collection class:
Typically, you should declare collection macros in a service provider.

## Methods

| Method | |
|--|--|
| [`all()`] | The all method returns the underlying array represented by the collection |
| [`average()`] | Alias for the avg method. |
| [`avg()`] | The avg method returns the average value of a given key: |
| [`chunk()`] | The chunk method breaks the collection into multiple, smaller collections of a given size:<br><br> This method is especially useful in views when working with a grid system such as Bootstrap. Imagine you have a collection of Eloquent models you want to display in a grid: |
| [`collapse()`] | The collapse method collapses a collection of arrays into a single, flat collection: |
| [`combine()`] | The combine method combines the values of the collection, as keys, with the values of another array or collection: |
| [`concat()`] | The concat method appends the given array or collection values onto the end of the collection: |
| [`contains()`] | The contains method determines whether the collection contains a given item:<br><br> You may also pass a key / value pair to the contains method, which will determine if the given pair exists in the collection:<br><br> Finally, you may also pass a callback to the contains method to perform your own truth test:<br><br> The contains method uses "loose" comparisons when checking item values, meaning a string with an integer value will be considered equal to an integer of the same value. Use the containsStrict method to filter using "strict" comparisons.<br><br> | [`containsStrict()`] | This method has the same signature as the contains method; however, all values are compared using "strict" comparisons. |
| [`count()`] | The count method returns the total number of items in the collection: |
| [`countBy()`] | The countBy method counts the occurrences of values in the collection. By default, the method counts the occurrences of every element:<br><br> However, you pass a callback to the countBy method to count all items by a custom value: |
| [`crossJoin()`] | The crossJoin method cross joins the collection's values among the given arrays or collections, returning a Cartesian product with all possible permutations: |
| [`dd()`] | The dd method dumps the collection's items and ends execution of the script:<br><br> If you do not want to stop executing the script, use the dump method instead. |
| [`diff()`] | The diff method compares the collection against another collection or a plain PHP array based on its values. This method will return the values in the original collection that are not present in the given collection: |
| [`diffAssoc()`] | The diffAssoc method compares the collection against another collection or a plain PHP array based on its keys and values. This method will return the key / value pairs in the original collection that are not present in the given collection: |
| [`diffKeys()`] | The diffKeys method compares the collection against another collection or a plain PHP array based on its keys. This method will return the key / value pairs in the original collection that are not present in the given collection: |
| [`dump()`] | The dump method dumps the collection's items:<br><br> If you want to stop executing the script after dumping the collection, use the dd method instead. |
| [`duplicates()`] | the duplicates method retrieves and returns duplicate values from the collection: |
| [`each()`] | The each method iterates over the items in the collection and passes each item to a callback:<br><br> If you would like to stop iterating through the items, you may return false from your callback: |
| [`eachSpread()`] | The eachSpread method iterates over the collection's items, passing each nested item value into the given callback:<br><br> You may stop iterating through the items by returning false from the callback: |
| [`every()`] | The every method may be used to verify that all elements of a collection pass a given truth test:<br><br> If the collection is empty, every will return true: |
| [`except()`] | The except method returns all items in the collection except for those with the specified keys:<br><br> For the inverse of except, see the only method. |
| [`filter()`] | The filter method filters the collection using the given callback, keeping only those items that pass a given truth test:<br><br> If no callback is supplied, all entries of the collection that are equivalent to false will be removed:<br><br> For the inverse of filter, see the reject method. |
| [`first()`] | The first method returns the first element in the collection that passes a given truth test:<br><br> You may also call the first method with no arguments to get the first element in the collection. If the collection is empty, null is returned: |
| [`firstWhere()`] | The firstWhere method returns the first element in the collection with the given key / value pair:<br><br> You may also call the firstWhere method with an operator:<br><br> Like the where method, you may pass one argument to the firstWhere method. In this scenario, the firstWhere method will return the first item where the given item key's value is "truthy": |
| [`flatMap()`] | The flatMap method iterates through the collection and passes each value to the given callback. The callback is free to modify the item and return it, thus forming a new collection of modified items. Then, the array is flattened by a level: |
| [`flatten()`] | The flatten method flattens a multi-dimensional collection into a single dimension:<br><br> You may optionally pass the function a "depth" argument:<br><br> In this example, calling flatten without providing the depth would have also flattened the nested arrays, resulting in ['iPhone 6S', 'Apple', 'Galaxy S7', 'Samsung']. Providing a depth allows you to restrict the levels of nested arrays that will be flattened. |
| [`flip()`] | The flip method swaps the collection's keys with their corresponding values: |
| [`forget()`] | The forget method removes an item from the collection by its key: <br><br> Unlike most other collection methods, forget does not return a new modified collection; it modifies the collection it is called on. |
| [`forPage()`] | The forPage method returns a new collection containing the items that would be present on a given page number. The method accepts the page number as its first argument and the number of items to show per page as its second argument: |
| [`get()`] | The get method returns the item at a given key. If the key does not exist, null is returned:<br><br> You may optionally pass a default value as the second argument:<br><br> You may even pass a callback as the default value. The result of the callback will be returned if the specified key does not exist: |
| [`groupBy()`] | The groupBy method groups the collection's items by a given key:<br><br> Instead of passing a string key, you may pass a callback. The callback should return the value you wish to key the group by:<br><br> Multiple grouping criteria may be passed as an array. Each array element will be applied to the corresponding level within a multi-dimensional array: |
| [`has()`] | The has method determines if a given key exists in the collection: |
| [`implode()`] | The implode method joins the items in a collection. Its arguments depend on the type of items in the collection. If the collection contains arrays or objects, you should pass the key of the attributes you wish to join, and the "glue" string you wish to place between the values:<br><br> If the collection contains simple strings or numeric values, pass the "glue" as the only argument to the method: |
| [`intersect()`] | The intersect method removes any values from the original collection that are not present in the given array or collection. The resulting collection will preserve the original collection's keys: |
| [`intersectByKeys()`] | The intersectByKeys method removes any keys from the original collection that are not present in the given array or collection: |
| [`isEmpty()`] | The isEmpty method returns true if the collection is empty; otherwise, false is returned: |
| [`isNotEmpty()`] | The isNotEmpty method returns true if the collection is not empty; otherwise, false is returned: |
| [`join()`] | The join method joins the collection's values with a string: |
| [`keyBy()`] | The keyBy method keys the collection by the given key. If multiple items have the same key, only the last one will appear in the new collection:<br><br> You may also pass a callback to the method. The callback should return the value to key the collection by: |
| [`keys()`] | The keys method returns all of the collection's keys: |
| [`last()`] | The last method returns the last element in the collection that passes a given truth test:<br><br> You may also call the last method with no arguments to get the last element in the collection. If the collection is empty, null is returned: |
| [`macro()`] | The static macro method allows you to add methods to the Collection class at run time. Refer to the documentation on extending collections for more information. |
| [`make()`] | The static make method creates a new collection instance. See the Creating Collections section. |
| [`map()`] | The map method iterates through the collection and passes each value to the given callback. The callback is free to modify the item and return it, thus forming a new collection of modified items:<br><br> Like most other collection methods, map returns a new collection instance; it does not modify the collection it is called on. If you want to transform the original collection, use the transform method. |
| [`mapInto()`] | The mapInto() method iterates over the collection, creating a new instance of the given class by passing the value into the constructor: |
| [`mapSpread()`] | The mapSpread method iterates over the collection's items, passing each nested item value into the given callback. The callback is free to modify the item and return it, thus forming a new collection of modified items: |
| [`mapToGroups()`] | The mapToGroups method groups the collection's items by the given callback. The callback should return an associative array containing a single key / value pair, thus forming a new collection of grouped values: |
| [`mapWithKeys()`] | The mapWithKeys method iterates through the collection and passes each value to the given callback. The callback should return an associative array containing a single key / value pair: |
| [`max()`] | The max method returns the maximum value of a given key: |
| [`median()`] | The median method returns the median value of a given key: |
| [`merge()`] | The merge method merges the given array or collection with the original collection. If a string key in the given items matches a string key in the original collection, the given items's value will overwrite the value in the original collection:<br><br> If the given items's keys are numeric, the values will be appended to the end of the collection: |
| [`min()`] | The min method returns the minimum value of a given key: |
| [`mode()`] | The mode method returns the mode value of a given key: |
| [`nth()`] | The nth method creates a new collection consisting of every n-th element:<br><br> You may optionally pass an offset as the second argument: |
| [`only()`] | The only method returns the items in the collection with the specified keys:<br><br> For the inverse of only, see the except method.<br><br> | [`pad()`] | The pad method will fill the array with the given value until the array reaches the specified size. This method behaves like the array_pad PHP function.<br><br> To pad to the left, you should specify a negative size. No padding will take place if the absolute value of the given size is less than or equal to the length of the array: |
| [`partition()`] | The partition method may be combined with the list PHP function to separate elements that pass a given truth test from those that do not: |
| [`pipe()`] | The pipe method passes the collection to the given callback and returns the result: |
| [`pluck()`] | The pluck method retrieves all of the values for a given key:<br><br> You may also specify how you wish the resulting collection to be keyed:<br><br> If duplicate keys exist, the last matching element will be inserted into the plucked collection: |
| [`pop()`] | The pop method removes and returns the last item from the collection: |
| [`prepend()`] | The prepend method adds an item to the beginning of the collection:<br><br> You may also pass a second argument to set the key of the prepended item: |
| [`pull()`] | The pull method removes and returns an item from the collection by its key: |
| [`push()`] | The push method appends an item to the end of the collection: |
| [`put()`] | The put method sets the given key and value in the collection: |
| [`random()`] | The random method returns a random item from the collection:<br><br> You may optionally pass an integer to random to specify how many items you would like to randomly retrieve. A collection of items is always returned when explicitly passing the number of items you wish to receive:<br><br> If the Collection has fewer items than requested, the method will throw an InvalidArgumentException. |
| [`reduce()`] | The reduce method reduces the collection to a single value, passing the result of each iteration into the subsequent iteration:<br><br> The value for $carry on the first iteration is null; however, you may specify its initial value by passing a second argument to reduce: |
| [`reject()`] | The reject method filters the collection using the given callback. The callback should return true if the item should be removed from the resulting collection:<br><br> For the inverse of the reject method, see the filter method. |
| [`reverse()`] | The reverse method reverses the order of the collection's items, preserving the original keys: |
| [`search()`] | The search method searches the collection for the given value and returns its key if found. If the item is not found, false is returned.<br><br> The search is done using a "loose" comparison, meaning a string with an integer value will be considered equal to an integer of the same value. To use "strict" comparison, pass true as the second argument to the method:<br><br> Alternatively, you may pass in your own callback to search for the first item that passes your truth test: |
| [`shift()`] | The shift method removes and returns the first item from the collection: |
| [`shuffle()`] | The shuffle method randomly shuffles the items in the collection: |
| [`slice()`] | The slice method returns a slice of the collection starting at the given index:<br><br> If you would like to limit the size of the returned slice, pass the desired size as the second argument to the method:<br><br> The returned slice will preserve keys by default. If you do not wish to preserve the original keys, you can use the values method to reindex them. |
| [`some()`] | Alias for the contains method. |
| [`sort()`] | The sort method sorts the collection. The sorted collection keeps the original array keys, so in this example we'll use the values method to reset the keys to consecutively numbered indexes:<br><br> If your sorting needs are more advanced, you may pass a callback to sort with your own algorithm. Refer to the PHP documentation on uasort, which is what the collection's sort method calls under the hood.<br><br> If you need to sort a collection of nested arrays or objects, see the sortBy and sortByDesc methods. |
| [`sortBy()`] | The sortBy method sorts the collection by the given key. The sorted collection keeps the original array keys, so in this example we'll use the values method to reset the keys to consecutively numbered indexes:<br><br> You can also pass your own callback to determine how to sort the collection values: |
| [`sortByDesc()`] | This method has the same signature as the sortBy method, but will sort the collection in the opposite order. |
| [`sortKeys()`] | The sortKeys method sorts the collection by the keys of the underlying associative array: |
| [`sortKeysDesc()`] | This method has the same signature as the sortKeys method, but will sort the collection in the opposite order.<br><br> | [`splice()`] | The splice method removes and returns a slice of items starting at the specified index:<br><br> You may pass a second argument to limit the size of the resulting chunk:<br><br> In addition, you can pass a third argument containing the new items to replace the items removed from the collection: |
| [`split()`] | The split method breaks a collection into the given number of groups: |
| [`sum()`] | The sum method returns the sum of all items in the collection:<br><br> If the collection contains nested arrays or objects, you should pass a key to use for determining which values to sum:<br><br> In addition, you may pass your own callback to determine which values of the collection to sum: |
| [`take()`] | The take method returns a new collection with the specified number of items:<br><br> You may also pass a negative integer to take the specified amount of items from the end of the collection: |
| [`tap()`] | The tap method passes the collection to the given callback, allowing you to "tap" into the collection at a specific point and do something with the items while not affecting the collection itself: |
| [`times()`] | The static times method creates a new collection by invoking the callback a given amount of times:<br><br> This method can be useful when combined with factories to create Eloquent models: |
| [`toArray()`] | The toArray method converts the collection into a plain PHP array. If the collection's values are Eloquent models, the models will also be converted to arrays: toArray also converts all of the collection's nested objects that are an instance of Arrayable to an array. If you want to get the raw underlying array, use the all method instead.<br><br> | [`toJson()`] | The toJson method converts the collection into a JSON serialized string: |
| [`transform()`] | The transform method iterates over the collection and calls the given callback with each item in the collection. The items in the collection will be replaced by the values returned by the callback: <br><br>Unlike most other collection methods, transform modifies the collection itself. If you wish to create a new collection instead, use the map method. |
| [`union()`] | The union method adds the given array to the collection. If the given array contains keys that are already in the original collection, the original collection's values will be preferred: |
| [`unique()`] | The unique method returns all of the unique items in the collection. The returned collection keeps the original array keys, so in this example we'll use the values method to reset the keys to consecutively numbered indexes:<br><br> When dealing with nested arrays or objects, you may specify the key used to determine uniqueness:<br><br> You may also pass your own callback to determine item uniqueness:<br><br> The unique method uses "loose" comparisons when checking item values, meaning a string with an integer value will be considered equal to an integer of the same value. Use the uniqueStrict method to filter using "strict" comparisons. |
| [`uniqueStrict()`] | This method has the same signature as the unique method; however, all values are compared using "strict" comparisons.<br><br> | [`unless()`] | The unless method will execute the given callback unless the first argument given to the method evaluates to true:<br><br> For the inverse of unless, see the when method. |
| [`unlessEmpty()`] | Alias for the whenNotEmpty method. |
| [`unlessNotEmpty()`] | Alias for the whenEmpty method. |
| [`unwrap()`] | The static unwrap method returns the collection's underlying items from the given value when applicable: |
| [`values()`] | The values method returns a new collection with the keys reset to consecutive integers: |
| [`when()`] | The when method will execute the given callback when the first argument given to the method evaluates to true:<br><br> For the inverse of when, see the unless method. |
| [`whenEmpty()`] | The whenEmpty method will execute the given callback when the collection is empty:<br><br> For the inverse of whenEmpty, see the whenNotEmpty method. |
| [`whenNotEmpty()`] | The whenNotEmpty method will execute the given callback when the collection is not empty:<br><br> For the inverse of whenNotEmpty, see the whenEmpty method. |
| [`where()`] | The where method filters the collection by a given key / value pair:<br><br> The where method uses "loose" comparisons when checking item values, meaning a string with an integer value will be considered equal to an integer of the same value. Use the whereStrict method to filter using "strict" comparisons. |
| [`whereStrict()`] | This method has the same signature as the where method; however, all values are compared using "strict" comparisons. |
| [`whereBetween()`] | The whereBetween method filters the collection within a given range: |
| [`whereIn()`] | The whereIn method filters the collection by a given key / value contained within the given array:<br><br> The whereIn method uses "loose" comparisons when checking item values, meaning a string with an integer value will be considered equal to an integer of the same value. Use the whereInStrict method to filter using "strict" comparisons. |
| [`whereInStrict()`] | This method has the same signature as the whereIn method; however, all values are compared using "strict" comparisons. |
| [`whereInstanceOf()`] | The whereInstanceOf method filters the collection by a given class type: |
| [`whereNotBetween()`] | The whereNotBetween method filters the collection within a given range: |
| [`whereNotIn()`] | The whereNotIn method filters the collection by a given key / value not contained within the given array:<br><br> The whereNotIn method uses "loose" comparisons when checking item values, meaning a string with an integer value will be considered equal to an integer of the same value. Use the whereNotInStrict method to filter using "strict" comparisons. |
| [`whereNotInStrict()`] | This method has the same signature as the whereNotIn method; however, all values are compared using "strict" comparisons. |
| [`wrap()`] | The static wrap method wraps the given value in a collection when applicable: |
| [`zip()`] | The zip method merges together the values of the given array with the values of the original collection at the corresponding index: |

## Higher Order Messages
Collections also provide support for "higher order messages", which are short-cuts for performing common actions on collections. The collection methods that provide higher order messages are: average, avg, contains, each, every, filter, first, flatMap, groupBy, keyBy, map, max, min, partition, reject, some, sortBy, sortByDesc, sum, and unique.
Each higher order message can be accessed as a dynamic property on a collection instance. For instance, let's use the each higher order message to call a method on each object within a collection:
Likewise, we can use the sum higher order message to gather the total number of "votes" for a collection of users:

[`all()`]: https://laravel.com/docs/5.8/collections#method-all
[`average()`]: https://laravel.com/docs/5.8/collections#method-average
[`avg()`]: https://laravel.com/docs/5.8/collections#method-avg
[`chunk()`]: https://laravel.com/docs/5.8/collections#method-chunk
[`collapse()`]: https://laravel.com/docs/5.8/collections#method-collapse
[`combine()`]: https://laravel.com/docs/5.8/collections#method-combine
[`concat()`]: https://laravel.com/docs/5.8/collections#method-concat
[`contains()`]: https://laravel.com/docs/5.8/collections#method-contains
[`containsStrict()`]: https://laravel.com/docs/5.8/collections#method-containsstrict
[`count()`]: https://laravel.com/docs/5.8/collections#method-count
[`countBy()`]: https://laravel.com/docs/5.8/collections#method-countBy
[`crossJoin()`]: https://laravel.com/docs/5.8/collections#method-crossjoin
[`dd()`]: https://laravel.com/docs/5.8/collections#method-dd
[`diff()`]: https://laravel.com/docs/5.8/collections#method-diff
[`diffAssoc()`]: https://laravel.com/docs/5.8/collections#method-diffassoc
[`diffKeys()`]: https://laravel.com/docs/5.8/collections#method-diffkeys
[`dump()`]: https://laravel.com/docs/5.8/collections#method-dump
[`duplicates()`]: https://laravel.com/docs/5.8/collections#method-duplicates
[`duplicatesStrict()`]: https://laravel.com/docs/5.8/collections#method-duplicatesstrict
[`each()`]: https://laravel.com/docs/5.8/collections#method-each
[`eachSpread()`]: https://laravel.com/docs/5.8/collections#method-eachspread
[`every()`]: https://laravel.com/docs/5.8/collections#method-every
[`except()`]: https://laravel.com/docs/5.8/collections#method-except
[`filter()`]: https://laravel.com/docs/5.8/collections#method-filter
[`first()`]: https://laravel.com/docs/5.8/collections#method-first
[`firstWhere()`]: https://laravel.com/docs/5.8/collections#method-first-where
[`flatMap()`]: https://laravel.com/docs/5.8/collections#method-flatmap
[`flatten()`]: https://laravel.com/docs/5.8/collections#method-flatten
[`flip()`]: https://laravel.com/docs/5.8/collections#method-flip
[`forget()`]: https://laravel.com/docs/5.8/collections#method-forget
[`forPage()`]: https://laravel.com/docs/5.8/collections#method-forpage
[`get()`]: https://laravel.com/docs/5.8/collections#method-get
[`groupBy()`]: https://laravel.com/docs/5.8/collections#method-groupby
[`has()`]: https://laravel.com/docs/5.8/collections#method-has
[`implode()`]: https://laravel.com/docs/5.8/collections#method-implode
[`intersect()`]: https://laravel.com/docs/5.8/collections#method-intersect
[`intersectByKeys()`]: https://laravel.com/docs/5.8/collections#method-intersectbykeys
[`isEmpty()`]: https://laravel.com/docs/5.8/collections#method-isempty
[`isNotEmpty()`]: https://laravel.com/docs/5.8/collections#method-isnotempty
[`join()`]: https://laravel.com/docs/5.8/collections#method-join
[`keyBy()`]: https://laravel.com/docs/5.8/collections#method-keyby
[`keys()`]: https://laravel.com/docs/5.8/collections#method-keys
[`last()`]: https://laravel.com/docs/5.8/collections#method-last
[`macro()`]: https://laravel.com/docs/5.8/collections#method-macro
[`make()`]: https://laravel.com/docs/5.8/collections#method-make
[`map()`]: https://laravel.com/docs/5.8/collections#method-map
[`mapInto()`]: https://laravel.com/docs/5.8/collections#method-mapinto
[`mapSpread()`]: https://laravel.com/docs/5.8/collections#method-mapspread
[`mapToGroups()`]: https://laravel.com/docs/5.8/collections#method-maptogroups
[`mapWithKeys()`]: https://laravel.com/docs/5.8/collections#method-mapwithkeys
[`max()`]: https://laravel.com/docs/5.8/collections#method-max
[`median()`]: https://laravel.com/docs/5.8/collections#method-median
[`merge()`]: https://laravel.com/docs/5.8/collections#method-merge
[`mergeRecursive()`]: https://laravel.com/docs/5.8/collections#method-mergerecursive
[`min()`]: https://laravel.com/docs/5.8/collections#method-min
[`mode()`]: https://laravel.com/docs/5.8/collections#method-mode
[`nth()`]: https://laravel.com/docs/5.8/collections#method-nth
[`only()`]: https://laravel.com/docs/5.8/collections#method-only
[`pad()`]: https://laravel.com/docs/5.8/collections#method-pad
[`partition()`]: https://laravel.com/docs/5.8/collections#method-partition
[`pipe()`]: https://laravel.com/docs/5.8/collections#method-pipe
[`pluck()`]: https://laravel.com/docs/5.8/collections#method-pluck
[`pop()`]: https://laravel.com/docs/5.8/collections#method-pop
[`prepend()`]: https://laravel.com/docs/5.8/collections#method-prepend
[`pull()`]: https://laravel.com/docs/5.8/collections#method-pull
[`push()`]: https://laravel.com/docs/5.8/collections#method-push
[`put()`]: https://laravel.com/docs/5.8/collections#method-put
[`random()`]: https://laravel.com/docs/5.8/collections#method-random
[`reduce()`]: https://laravel.com/docs/5.8/collections#method-reduce
[`reject()`]: https://laravel.com/docs/5.8/collections#method-reject
[`replace()`]: https://laravel.com/docs/5.8/collections#method-replace
[`replaceRecursive()`]: https://laravel.com/docs/5.8/collections#method-replacerecursive
[`reverse()`]: https://laravel.com/docs/5.8/collections#method-reverse
[`search()`]: https://laravel.com/docs/5.8/collections#method-search
[`shift()`]: https://laravel.com/docs/5.8/collections#method-shift
[`shuffle()`]: https://laravel.com/docs/5.8/collections#method-shuffle
[`slice()`]: https://laravel.com/docs/5.8/collections#method-slice
[`some()`]: https://laravel.com/docs/5.8/collections#method-some
[`sort()`]: https://laravel.com/docs/5.8/collections#method-sort
[`sortBy()`]: https://laravel.com/docs/5.8/collections#method-sortby
[`sortByDesc()`]: https://laravel.com/docs/5.8/collections#method-sortbydesc
[`sortKeys()`]: https://laravel.com/docs/5.8/collections#method-sortkeys
[`sortKeysDesc()`]: https://laravel.com/docs/5.8/collections#method-sortkeysdesc
[`splice()`]: https://laravel.com/docs/5.8/collections#method-splice
[`split()`]: https://laravel.com/docs/5.8/collections#method-split
[`sum()`]: https://laravel.com/docs/5.8/collections#method-sum
[`take()`]: https://laravel.com/docs/5.8/collections#method-take
[`tap()`]: https://laravel.com/docs/5.8/collections#method-tap
[`times()`]: https://laravel.com/docs/5.8/collections#method-times
[`toArray()`]: https://laravel.com/docs/5.8/collections#method-toarray
[`toJson()`]: https://laravel.com/docs/5.8/collections#method-tojson
[`transform()`]: https://laravel.com/docs/5.8/collections#method-transform
[`union()`]: https://laravel.com/docs/5.8/collections#method-union
[`unique()`]: https://laravel.com/docs/5.8/collections#method-unique
[`uniqueStrict()`]: https://laravel.com/docs/5.8/collections#method-uniquestrict
[`unless()`]: https://laravel.com/docs/5.8/collections#method-unless
[`unlessEmpty()`]: https://laravel.com/docs/5.8/collections#method-unlessempty
[`unlessNotEmpty()`]: https://laravel.com/docs/5.8/collections#method-unlessnotempty
[`unwrap()`]: https://laravel.com/docs/5.8/collections#method-unwrap
[`values()`]: https://laravel.com/docs/5.8/collections#method-values
[`when()`]: https://laravel.com/docs/5.8/collections#method-when
[`whenEmpty()`]: https://laravel.com/docs/5.8/collections#method-whenempty
[`whenNotEmpty()`]: https://laravel.com/docs/5.8/collections#method-whennotempty
[`where()`]: https://laravel.com/docs/5.8/collections#method-where
[`whereStrict()`]: https://laravel.com/docs/5.8/collections#method-wherestrict
[`whereBetween()`]: https://laravel.com/docs/5.8/collections#method-wherebetween
[`whereIn()`]: https://laravel.com/docs/5.8/collections#method-wherein
[`whereInStrict()`]: https://laravel.com/docs/5.8/collections#method-whereinstrict
[`whereInstanceOf()`]: https://laravel.com/docs/5.8/collections#method-whereinstanceof
[`whereNotBetween()`]: https://laravel.com/docs/5.8/collections#method-wherenotbetween
[`whereNotIn()`]: https://laravel.com/docs/5.8/collections#method-wherenotin
[`whereNotInStrict()`]: https://laravel.com/docs/5.8/collections#method-wherenotinstrict
[`wrap()`]: https://laravel.com/docs/5.8/collections#method-wrap
[`zip()`]: https://laravel.com/docs/5.8/collections#method-zip
