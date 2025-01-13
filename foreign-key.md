create table post(
	id SERIAL primary key,
	name VARCHAR(255),
	content text,
	user_id INT,
	CONSTRANT fk_user
		foreign key(user_id)
			references "user"(id)
);
