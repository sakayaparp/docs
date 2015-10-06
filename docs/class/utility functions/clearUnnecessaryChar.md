### **clearUnnecessaryChar()**
##### Description :
> xxx

##### Code :
```php
/**
*/
public static function clearUnnecessaryChar(&$texts)
{
	$replace = function(&$text)
	{
		$text = trim($text);
		$text = str_replace(array(chr(9), chr(10), chr(13), chr(160)), '', $text);
		$text = preg_replace("#\s{2,}#", ' ', $text);
	};

	if(is_array($texts))
	{
		foreach ($texts as $name => &$text)
		{
			$replace($text);
		}	
	}
	else
	{
		$replace($texts);
	}
}
```

##### Example :
> Example 1:
```php
```

> Example 2:
```php
```

##### Notes :
```
```