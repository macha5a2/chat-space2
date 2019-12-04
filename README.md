# README

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|username|string|null: false|

### Association
- has_many :groups_users
- has_many :messages

## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|group_name|integer|null: false|

### Association
- has_many :groups_users
- has_many :message

## messageテーブル
|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|image|text||

### Association
- belongs_to :group
- belongs_to :user
