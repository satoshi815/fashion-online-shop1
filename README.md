# fashion-online-shop DB設計

***
## users
|Column|Type|Options|
|------|----|-------|
|nickname|string|null:false|
|email|string|null:false|
|password|string|null:false|
|family_name|string|null:false|
|last_name|string|null:false|
|furigana_family_name|string|null:false|
|furigana_last_name|string|null:false|
|phone_namber|integer|null:false|
|birthday_year|integer|null:false|
|birthday_month|integer|null:false|
|birthday_day|integer|null:false|

### Association
- has_one address

***
## items
|Column|Type|Options|
|------|----|-------|
|name|string|null:false|
|description|text|null:false|
|price|integer|null:false|
|size|string|null:false|
|material|string|null:false|

### Association
- has_many images

***
## images
|Column|Type|Options|
|------|----|-------|
|image|string|null:false|
|item_id|integer|null:false|

### Association
- belongs_to item

***
## addresses
|Column|Type|Options|
|------|----|-------|
|postal_code|integer|null:false|
|prefectures|string|null:false|
|city|string|null:false|
|street|string|null:false|
|building|string|null:false|
|user_id|integer|null:false|

### Association
- belongs_to user

***