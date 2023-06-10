# SQL HW 1

```
 CREATE TABLE employees(
  id serial PRIMARY KEY,
  employee_name varchar(50) not null
);

select * from employees;

insert into employees(employee_name)
values ('Anna'),
    ('Arina'),
    ('Irina'),
    ('Alena'),
    ('Elena'),
    ('Arina'),
    ('Irina'),
    ('Matvey'),
    ('Petr'),
    ('Artiom'),
    ('Alexey'),
    ('Alexandr'),
    ('Ivan'),
    ('Arina'),
    ('Irina'),
    ('Alena'),
    ('Elena'),
    ('Arina'),
    ('Irina'),
    ('Alena'),
    ('Ivan'),
    ('Mihail'),
    ('Ilya'),
    ('Andrey'),
    ('Maryia'),
    ('Anfisa'),
    ('Vladislav'),
    ('Miron'),
    ('Oleg'),
    ('Tanya'),
    ('Maksim'),
    ('Daniil'),
    ('Katya'),
    ('Margarita'),
    ('Natasha'),
    ('Tamara'),
    ('Ludmila'),
    ('Kristina'),
    ('Inna'),
    ('Polina'),
    ('Anastasiya'),
    ('Viktoryia'),
    ('Gayaniya'),
    ('Eva'),
    ('Mark'),
    ('Kirill'),
    ('Emma'),
    ('Karina'),
    ('Marta'),
    ('Olga'),   
    ('Svetlana'),
    ('Yana'),
    ('Darya'),
    ('Vladislava'),
    ('Galina'),
    ('Veronika'),
    ('Arseniy'),
    ('Alla'),
    ('Artur'),
    ('Bogdan'),  
    ('Vadim'),
    ('Vasiliy'),
    ('Vladimir'),
    ('Boris'),
    ('Denis'),
    ('Elizaveta'),
    ('Zhanna'),
    ('Ignat'),
    ('Timofey'),
    ('Marina');

 CREATE table salary(
   id serial primary key,
   monthly_salary  Int not null 
  );
     
 select * from salary
 
 insert into salary(monthly_salary)
 values (1000),
(1100),
(1200),
(1300),
(1400),
(1500),
(1600),
(1700),
(1800),
(1900),
(2000),
(2100),
(2200),
(2300),
(2400),
(2500);

 create table employee_salary(
 id serial  primary key,
  employee_id Int unique not null ,
  salary_id Int not null
 );
 
select * from employee_salary

insert into employee_salary(employee_id, salary_id)
values (3,7),
(1,4),
(5,9),
(40,13),
(23,4),
(11,2),
(52,10),
(19,13),
(26,4),
(16,1),
(30,7),
(72,7),
(22,16),
(73,16),
(65,11),
(74,5),
(71,11),
(81,9),
(12,13),
(90,12),
(21,10),
(29,4),
(27,1),
(2,13),
(4,15),
(7,17),
(6,6),
(8,8),
(9,19),
(10,10),
(13,2),
(75,7),
(80,11),
(34,9),
(99,12),
(77,14),
(14,14),
(15,15),
(17,1),
(24,13);


 create table roles(
 id serial  primary key,
  role_name int not null unique
 );
 
select * from roles;

alter table roles alter column role_name type varchar(30);

insert into roles (role_name)
values ('Junior Python developer'),
('Middle Python developer'),
('Senior Python developer'),
('Junior Java developer'),
('Middle Java developer'),
('Senior Java developer'),
('Junior JavaScript developer'),
('Middle JavaScript developer'),
('Senior JavaScript developer'),
('Junior Manual QA engineer'),
('Middle Manual QA engineer'),
('Senior Manual QA engineer'),
('Project Manager'),
('Designer'),
('HR'),
('CEO'),
('Sales manager'),
('Junior Automation QA engineer'),
('Middle Automation QA engineer'),
('Senior Automation QA engineer');


create table roles_employee (
id Serial  primary key,
employee_id Int unique not null ,
role_id Int not null ,
foreign key(employee_id) references employees(id),
foreign key(role_id) references roles(id)
);

select * from roles_employee;

	insert into roles_employee (employee_id, role_id)
values (7,2),
       (20,4),
       (3,9),
       (5,13),
       (23,4),
       (31,2),
       (10,9),
       (26,13),
       (21,3),
       (34,4),
       (6,7),
       (1,5),
       (11,1),
       (8,10),
       (2,11),
       (14,12),
       (4,20),
       (9,1),
       (12,12),
       (13,14),
       (18,13),
        (15,7),
       (16,18),
       (27,8),
       (41,4),
       (30,1),
       (22,2),
       (17,4),
       (33,3),
       (28,16),
       (39,17),
        (19,13),
       (36,14),
       (35,15),
       (37,15),
       (24,16),
       (29,18),
       (38,17),
       (40,18),
       (32,19),
       (25,20);
 ```
