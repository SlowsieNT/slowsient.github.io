# paginate.js
## This is free and unencumbered software released into the public domain.
Made to work with IE6.<br>
Library is feature rich.<br>
```html
<!-- Best to download js file copy -->
<script src="https://slowsient.github.io/js/lib/paginate.js"></script>
```
## Code samples:
```js
// Pagination Example code:
var pag1 = Paginate({
	iPageNum: 1, iPerPage: 2,
	// ALL PROPERTIES BELOW CAN BE WRITTEN IN camelCase, or PascalCase!
	// Data[0: DataType(0=Array, 1=Object), 1: ArrayOrObject]
	Data: [
		0, [1,2,3,4,5] // OR: [ 1, {a:1,b:2,c:3,d:4,e:5} ]
	],
	// OPTIONAL: Auto disable Next/Back button?
	AutoDisable: true,
	// OPTIONAL: ALL Properties below are Element, or Array-like (except Update callback, yes):
	Back: [back1, back2],
	Next: [next1, next2],
	// OPTIONAL: if INPUT/TEXTAREA/SELECT then user can modify them:
	PerPage: [perPage1, perPage2],
	CurPage: [curPage1, curPage2],
	PageCount: [pageNum1, pageNum2],
	// OPTIONAL: These are read only:
	PageItemsCount: [PageItemsCount1, PageItemsCount2],
	ItemsCount: [ItemsCount1, ItemsCount2],
	// Update usually called after any change
	Update: function (aPageItems, aPageItemsLen, aPerPage, aPageNum, aPageCount, aArrayLen) {
		// Write code here to render page items
		if ("undefined" !== typeof console)
			console.log(aPageItems);
	}
});
```