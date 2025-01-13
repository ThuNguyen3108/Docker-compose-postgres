create table "user"(
	id SERIAL primary key, -- INT -> +1
	name VARCHAR(255), -- VARCHAR = TEXT has a constraint on size
	email VARCHAR(255),
	password text,
	age INT 
);

insert into "user" (email, name, age, password) values ('troy@fake.email','Troy',
'26', 'abc123abc');


select * from "user";

select id, name, email from "user";

select * from "user" where age > 27;

select * from "user" where id = 1;

