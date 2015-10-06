### **getMonthFullName()**
##### Description :
> ใช้สำหรับดึงข้อมูลชื่อเดือนแบบเต็ม

##### Code :
```php
/**
* @param $month int Number of month
*/
public static function getMonthFullName($month)
{
	$months = array('January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 
		'October', 'November', 'December');

	if(empty($month))
		return $months;
	else
		return $months[$month - 1];
}
```

##### Example :
> Example 1:
```php
utility::getMonthFullName();

/* output
 array('January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 
		'October', 'November', 'December')
```

> Example 2:
```php
utility::getMonthFullName('1');

/* output
 January
```

##### Notes :
```
```