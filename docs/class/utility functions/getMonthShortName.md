### **getMonthShortName()**
##### Description :
> ใช้สำหรับดึงข้อมูลชื่อเดือนแบบย่อ

##### Code :
```php
/**
* @param $month int Number of month
*/
public static function getMonthShortName($month = '')
{
	$months = array('JAN', 'FEB', 'MAR', 'APR', 'MAY', 'JUN', 'JUL', 'AUG', 'SEP', 'OCT', 'NOV', 'DEC');
	
	if(empty($month))
		return $months;
	else
		return $months[$month - 1];
}
```

##### Example :
> Example 1:
```php
utility::getMonthShortName();

/* output
 array('JAN', 'FEB', 'MAR', 'APR', 'MAY', 'JUN', 'JUL', 'AUG', 'SEP', 'OCT', 'NOV', 'DEC')
```

> Example 2:
```php
utility::getMonthShortName('1');

/* output
 JAN
```

##### Notes :
```
```