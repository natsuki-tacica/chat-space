# README

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

## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## messages　テーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer| foreign_key: true|
|group_id|integer|foreign_key: true|
|image|string|
|body|text|

### Association
- belongs_to :group
- belongs_to :user

## user　テーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|name|integer|null: false|
|email|string|null: false|
|encrypted_password|string|null: false|

### Association
- has_many:messages
- has_many:groups_users

