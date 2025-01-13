create table post(
	id SERIAL primary key,
	name VARCHAR(255),
	content text,
	user_id INT,
	CONSTRAINT fk_user
		FOREIGN KEY(user_id)
			REFERENCES "user"(id)
);


![image](https://github.com/user-attachments/assets/95d2b2db-e4e7-49db-a773-7f702d171a96)
