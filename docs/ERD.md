Table users {
id uuid [primary key]
name varchar
phone_number varchar [unique]
created_at timestamp
updated_at timestamp
}

Table packages {
id uuid [primary key]
name varchar
duration integer
price integer
created_at timestamp
updated_at timestamp
}

Table payments {
id uuid [primary key]
user_id integer [ref: > users.id]
package_id integer [ref: > packages.id]
phone_number varchar
amount integer
status varchar
mpesa_transaction_code varchar [unique]
created_at timestamp
updated_at timestamp
}

Table sessions {
id uuid [primary key]
user_id uuid [ref: > users.id]
package_id uuid [ref: > packages.id]
payment_id uuid [ref: - payments.id, unique]
start_time timestamp
end_time timestamp
status varchar
created_at timestamp
updated_at timestamp
}

Table webhook_logs {
id uuid [primary key]
payment_id uuid [ref: > payments.id, null]
raw_payload jsonb
received_at timestamp
}

Table sms_logs {
id uuid [primary key]
session_id uuid [ref: > sessions.id, null]
phone_number varchar
message text
status varchar
provider_message_id varchar
created_at timestamp
updated_at timestamp
}

Table access_grant_logs {
id uuid [primary key]
session_id uuid [ref: > sessions.id]
status varchar
provider_response text
created_at timestamp
updated_at timestamp
}