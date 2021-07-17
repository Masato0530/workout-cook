# README

##　DB設計

## usersテーブル

| Column   | Type   | Options     |
| -------- | ------ | ----------- |
| email    | string | null: false |
| password | string | null: false |
| nickname | string | null: false |

## Association

- has_many :posts
- has_many :comments


## postsテーブル

| Column   | Type    | Options                        |
| -------- | ------  | ----------------------         |
| text     | text    |                                |
| image    | text    |                                |
| user_id  | integer | null: false, foreign_key: true |

## Association

- belongs_to :user
- belongs_to :comments

## comments テーブル

| Column   | Type    | Options                        |
| -------- | ------  | ----------------------         |
| text     | text    | null: false                    |
| user_id  | integer | null: false, foreign_key: true |
| post_id | integer | null: false, foreign_key: true  |

- belongs_to :post
- belongs_to :user
