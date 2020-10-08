# protpspace

# users テーブル

| Column      | Type   | Options     |
| ----------- | ------ | ----------- |
| name        | string | null: false |
| email       | string | null: false |
| password    | string | null: false |
| profile     | text   | null: false |
| occupation  | text   | null: false |
| position    | text   | null: false |

- has_many :prototypes
- has_many :comments

# commentsテーブル

| Column    | Type       | Options     |
| --------- | ---------- | ----------- |
| text      | text       | null: false |
| user      | references | null: false |
| prototype | references | null: false |

- belongs_to :prototype
- belongs_to :user


# prototypesテーブル

| Column        | Type       | Options     |
| ------------- | ---------- | ----------- |
| title         | string     | null: false |
| catch_copy    | text       | null: false |
| concept       | text       | null: false |
| image         | string     | null: false |
| user          | references | null: false |

- has_many :comments
- belongs_to :user