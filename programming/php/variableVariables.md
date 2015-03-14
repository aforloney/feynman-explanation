A _variable variables_ is a way of dynamically defining/using a variable within PHP.

Conventionally variables are defined as such,

```php
	$var = 'name';
```

When using _variable variables_, you can treat the string value of one variable as the name of another variable. This is done by preceding 
the variable with an extra dollar sign, 

```php
	$$var = 'anthony';
```

This will use the return value of `var` and define a variable dynamically as `name`.

```php
	// helpful visual of the above,
	// $($var) = 'anthony';
	//    ^
	//  'name' (PHP retrieves the contents of $var and converts the return value to a string, ie 'name')
	// 			=>
	// 				$name = 'anthony';
	//
	echo $var;	// returns 'name'
	echo $$var;	// returns 'anthony'
	echo $name;	// returns 'anthony'
```

This can even be extended further by adding another dollar sign,

```php
	$$$var = 'aforloney';
	// $$($var) = 'aforloney';
	//		^
	//    'name' (PHP retrieves the contents of $var and converts the return value to a string, ie 'name')
	// 			=>
	// 				$($name) = 'aforloney';
	//					^
	//				  'anthony'
	//						=>
	//							$anthony = 'aforloney';
	//
	echo $var;		// returns 'name'
	echo $$var;		// returns 'anthony'
	echo $$$var;	// returns 'aforloney'
	echo $anthony;	// returns 'aforloney'
```





