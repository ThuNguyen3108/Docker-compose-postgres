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

update "user" set email = 'thuthianhnguyen@gmail.com' where id = 1;


delete from "user" where id = 2;


![image](https://github.com/user-attachments/assets/c9b9186e-7978-4279-9be0-508c37b2d176)


