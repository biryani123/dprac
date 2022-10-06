DBMS PRACTICALS (QUERIES)
1) SQL STATEMENT 1-

--prac1a

select * from dept;

--prac1b

select * from emp where sal > 3000;

select ename,sal from emp;

select ename from emp;

select sal, sal+2000 from emp;

select ename, sal from emp where sal > 2000;

select ename,sal from emp where sal between 800 and 2000;

select * from emp where job in ('MARKETING','ANALYST','SALESMAN');

select * from emp where job = 'MANAGER' and sal = 2975;

select * from emp where ename like 'A%';

select * from emp where comm is null;

select*from emp;

--prac1c

select upper(ename),lower(ename),initcap(ename) from emp;

select lpad(ename,10,'*'), rpad(ename,10,'*') from emp;

--prac2a

Inner Join-

select ename,empno,dname,sal

from emp inner join dept

on emp.deptno = dept.deptno;

Equi Join-

select ename, empno, dname, sal

from emp, dept

where emp.deptno = dept.deptno;

--prac2b

select count(empno) from emp;

select sum(sal) from emp;

select avg(sal) from emp;

select min(sal) from emp;

select max(sal) from emp;

--prac4a

create table pp2(emp_no number(3) primary key, 

emp_lname varchar(15), 

emp_fname varchar(15) not null, 

emp_sal number(5), 

emp_hiredate date, 

job_code number(3) default'501');

insert into pp2 values(1,'Glasswala','Rehan',1000,'8-aug-2022','201');

insert into pp2 values(2,'Patel','Saad',1000,'8-aug-2022','301');

insert into pp2 values(3,'Pereira','Simeon',1000,'8-aug-2022','401');

alter table pp2 add emp_mobile number(10);

alter table pp2
drop column emp_mobile

select * from pp2;

--prac4b

create table pp2(emp_no number(3) primary key, 

emp_lname varchar(15), 

emp_fname varchar(15) not null, 

emp_sal number(5), 

emp_hiredate date, 

job_code number(3) default'501');

insert into pp2 values(1,'Glasswala','Rehan',1000,'8-aug-2022','201');

insert into pp2 values(2,'Patel','Saad',1000,'8-aug-2022','301');

select * from pp2;

--prac3a

create table student(rollno int, sname varchar(20), sclass varchar(10));

insert into student values(1,'shweta','syit');

insert into student values(2,'Rehan','syit');

select * from pp2;

--prac3b

delete from student where rollno = 3;

select * from student;

--prac3c

update student

set class='tyit'

where rollno=2;

select * from student;









