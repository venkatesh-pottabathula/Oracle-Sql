create table stu(Rno int primary key,name varchar(20),scl varchar(20));

insert into stu values(1,'james','svbv'),(2,'martin','brilliant'),(3,'david','srichaithyana');

select * from stu

alter table stu Drop constraint PK_stu;

alter table stu add primary key(name); 