## usersテーブル

| Column     | Type   | Option      |
| ---------- | ------ | ----------- |
| email      | string | null: false |
| password   | string | null: false |
| name       | string | null: false |
| profile    | text   | null: false |
| occupation | text   | null: false |
| position   | text   | null: false |

## Association

- has_many :prototype
- has_many :comments

## prototypesテーブル

| Column     | Type       | Option      |
| ---------- | ---------- | ----------- |
| title      | string     | null: false |
| catch_copy | text       | null: false |
| concept    | text       | null: false |
| image      |            |             |
| user       | references |             |

## Association

- has_many :comments
- belongs_to :user

## comments

| Column    | Type       | Option      |
| --------- | ---------- | ----------- |
| text      | text       | null: false |
| user      | references |             |
| prototype | references |             |

## Association

- belongs_to :user
- belongs_to :prototype