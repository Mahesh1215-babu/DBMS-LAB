create table employee1(emp_id int primary key,emp_name varchar(20),salary int,mobile_no int,dept char(8));

insert into employee1 values(101,'Alice',50000,12345678,'HR'),(102,'Bob',60000,23456789,'Finance'),(103,'Charlie',55000,34567890,'IT'),(104,'David',62000,45678901,'Sales'),(105,'Eve',48000,56789012,'Support'),(106,'Happy',50000,67890123,'Finance');

delimiter //

create function sum2()
returns decimal(10,2)
no sql
begin

declare totalsalaries decimal(10,2);
select sum(salary) into totalsalaries
from employee1
where dept='Finance';
return totalsalaries;
end //

delimiter ;

select sum2() as totalsalaries;
