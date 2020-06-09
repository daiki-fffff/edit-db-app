## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|username|string|null: false|
|password|string|null: false|

### Association
- has_many :messages
- has_many :posts

## Groupテーブル
|Column|Type|Options|
|------|----|-------|
|groupname|string|null: false|
|adduser|string|null: false|

### Association
- has_many :user
- has_many :message

## Group_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## messageテーブル
|Column|Type|Options|
|-------|----|-------|
|text|text|null: false|
|image|string|null: false|

### Association
- has_many :user