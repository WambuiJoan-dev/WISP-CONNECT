Table users {
id uuid [primary key]
name varchar [not null]
phone_number varchar [unique, not null]
created_at timestamp
updated_at timestamp
}

Table packages {
id uuid [primary key]
name varchar [not null]
duration integer [not null, note: 'minutes; must be > 0']
price integer [not null, note: 'must be > 0']
created_at timestamp
updated_at timestamp
}

Table payments {
id uuid [primary key]
user_id uuid [ref: > users.id, not null]
package_id uuid [ref: > packages.id, not null]
phone_number varchar [not null]
amount integer [not null, note: 'must be > 0']
status varchar [not null]
merchant_request_id varchar
checkout_request_id varchar [unique]
mpesa_transaction_code varchar
created_at timestamp
updated_at timestamp
}

Table sessions {
id uuid [primary key]
payment_id uuid [ref: - payments.id, unique, not null]
start_time timestamp [not null]
end_time timestamp [not null, note: 'must be > start_time']
status varchar [not null]
created_at timestamp
updated_at timestamp
}

Table webhook_logs {
id uuid [primary key]
payment_id uuid [ref: > payments.id]
raw_payload jsonb
received_at timestamp
}

Table sms_logs {
id uuid [primary key]
payment_id uuid [ref: > payments.id]
session_id uuid [ref: > sessions.id]
phone_number varchar [not null]
message text [not null]
status varchar [not null]
provider_message_id varchar
created_at timestamp
updated_at timestamp
}

Table access_grant_logs {
id uuid [primary key]
session_id uuid [ref: > sessions.id, not null]
mac_address varchar
duration_minutes integer [note: 'must be > 0']
status varchar [not null]
provider_response text
created_at timestamp
updated_at timestamp
}

Table ussd_interaction_logs {
id uuid [primary key]
user_id uuid [ref: > users.id]
phone_number varchar [not null]
session_id_ussd varchar
final_screen varchar
outcome varchar
started_at timestamp
ended_at timestamp
}