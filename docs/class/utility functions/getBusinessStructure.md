### **clearUnnecessaryChar()**
##### Description :
> xxx

##### Code :
```php
/**
*/
public static function getBusinessStructure($bustype, $options)
{
	$sql = static::getBusinessStructureSql($bustype, $options);
	$num = 0;
	$result = mysql_query($sql) or die( mysql_error() );
	while($data = mysql_fetch_array($result))
	{
		for($i=0;$i<mysql_num_fields($result);$i++)
		{
			$fieldName = mysql_field_name($result,$i);
			$structure[$num][$fieldName] = $data[$fieldName];
		}
		$num++;
	}

	return $structure;
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