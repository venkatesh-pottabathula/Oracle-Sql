create table seller(sid int primary key,sname varchar(30),scontact numeric(9,0));

insert into seller values(1,'virat',987657),(2,'dhoni',12345),(3,'jadeja',56789);

select * from seller

create table product(pid int foreign key references seller(sid)),pname varchar(20),pmake varchar(20),pmodel varchar(20));

insert into product values(1,'nikhil','phone','2020');

select s.sid,s.sname from seller as s right outer join product as p
                        on s.sid=p.pid
                        where s.sid is null
                        
select s.sid,s.sname from seller as s left outer join product as p
                        on s.sid=p.pid
                        where p.pid is null