##UserType

| Type | description |
|---|---|
| customer | customer of the system |
| admin | manager of the system |

## User

| Attribute | Data Type | Description | Constraints |
|---|---|---|---|
| user_id | serial | unique idendifier of user | Primary Key |
| firstname | varchar(255) | user's firstname | Not Null |
| surename | varchar(255) | user's surname | Not Null |
| phonenumber | varchar(10) | user's phonenumber | Not Null |
| user_type | UserType | role of the user | default: customer |

## Apponment

| Attributte | Data Type | Description | Constraints |
|---|---|---|---|
| appoointment_id | serial | unique identifier of appointment | primary key |
| broken_peart | varchar(255) | the part of the car that is broken and need to be fixed | None |
| short_description | varchar(255) | brief description of the sappointment | none |
| user_id | integer | user id of the user that created this appointment | Foreign key, not null |
| car_id | integer | car id of the car that needs fxixing | foreign key, Not Null |

## Car
| Attributte | Data Type | Description | Constraints |
|---|---|---|---|
| car_id | serial | unique of car | primary key |
| brand | varchar(255) | brand of the car | Not Null |
| model | varchar(255) | model of the car | Not Null |
| owner | integer | owner of the car | Not Null |
