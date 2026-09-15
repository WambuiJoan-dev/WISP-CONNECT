`Table users {
user_id integer [primary key]
name varchar
phone_number varchar [unique]
created_at timestamp
updated_at timestamp
}`

`Table packages {
package_id integer [primary key]
name varchar
duration integer
price integer
}`

`Table payments {
id integer [primary key]
phone_number varchar
amount integer
status varchar
mpesa_transaction_code varchar
created_at timestamp
updated_at timestamp
}`

`Table sessions {
id integer [primary key]
user_id integer [ref: > users.id]
package_id integer [ref: > packages.id]
payment_id integer [ref: - payments.id, unique]
start_time timestamp
end_time timestamp
status varchar
created_at timestamp
updated_at timestamp
}`

`Table webhook_logs {
id integer [primary key]
payment_id integer [ref: > payments.id, null]
raw_payload jsonb
received_at timestamp
}`