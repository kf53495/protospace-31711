# テーブル設計

## users テーブル

| Column     | Type   | Options     |
| :--------: | :----: | :---------: |
| email      | string | null: false |
| password   | string | mull: false |
| name       | string | mull: false |
| profile    | text   | mull: false |
| occupation | text   | mull: false |
| position   | text   | mull: false |

### Association

- has_many :prototypes
- has_many :comments


## prototypes テーブル

| Column     | Type       | Options     |
| :--------: | :--------: | :---------: |
| title      | string     | mull: false |
| catch_copy | text       | mull: false |
| concept    | text       | mull: false |
| image      | -          | -           |
| user       | references | -           |

### association

- belongs_to :user
- has_many :comments


## comments テーブル

| Column    | Type       | Options     |
| :-------: | :--------: | :---------: |
| text      | text       | mull: false |
| user      | references | -           |
| prototype | references | -           |

# Association

- belongs_to :user
- belongs_to :prototype