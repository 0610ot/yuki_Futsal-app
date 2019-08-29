# README

# データベース設計


## usersテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false, index true, unique: true|
|town|string|null: false|

### Association
- has_one :group
- has_many :messages
- has_many :user-group
- has_many :place


## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false, unique: true|
### Association
- has_many :messages
- has_many :user


## placesテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|town|string|null: false|
### Association
- has_one :user


## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|image|string| |
|user_id|references| null:false,foreign_key:true|
|group_id|references| null:false,foreign_key: true|
|content|text| |
### Association
- belongs_to :user
- belongs_to :groups

## users_groupsテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|references| null:false,foreign_key: true|
|group_id|references| null:false,foreign_key: true|
### Association
- belongs_to :user
- belongs_to :group

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

