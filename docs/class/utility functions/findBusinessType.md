### **findBusinessType()**
##### Description :
> xxx

##### Code :
```php
/**
* Use to find Business Type and Smart Shop by filter
* @param String $fieldNoneEmpty 
* @param String $filter 
* @return Mixed $businessTypes 
*/
public static function findBusinessType($fieldNoneEmpty, $filter)
{
	$businessTypes = array();
	$sql = "SELECT bu.BusinessType FROM (
		SELECT IF(sbu.OLMTrade = 'Y', 'Trade', 'OLM') AS BusinessType
			FROM smis_user AS su 
				INNER JOIN smis_businessunit AS sbu ON sbu.BusUnitID = su.BusUnitID 
				INNER JOIN smis_organise AS so ON so.BusOrgan = sbu.BusOrgan 
					WHERE " . $fieldNoneEmpty . "!='' " . $filter . ") AS bu
						GROUP BY bu.BusinessType";
	$result = mysql_query($sql);

	while($row = mysql_fetch_array($result))
	{
		$businessTypes[] = $row['BusinessType'];
	}

	return $businessTypes;
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