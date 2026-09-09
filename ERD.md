`Table users {
id integer [primary key]
name varchar
phone_number varchar [unique]
}`

`Table packages {
id integer [primary key]
name varchar
duration integer
price integer
}
`
`Table payments {
id integer [primary key]
phone_number varchar
amount integer
status varchar
mpesa_transaction_code varchar
timestamp timestamp
}`

`Table sessions {
id integer [primary key]
user_id integer [ref: > users.id]
package_id integer [ref: > packages.id]
payment_id integer [ref: - payments.id, unique]
start_time timestamp
end_time timestamp
status varchar
}`