DBMS PRACTICALS (QUERIES)
1) SQL STATEMENT 1-
--prac1a
create table dept(   
  deptno     number(2,0),   
  dname      varchar2(14),   
  loc        varchar2(13),   
  constraint pk_dept primary key (deptno)   
)
select * from dept;

--prac1b
create table emp(   
  empno    number(4,0),   
  ename    varchar2(10),   
  job      varchar2(9),   
  mgr      number(4,0),   
  hiredate date,   
  sal      number(7,2),   
  comm     number(7,2),   
  deptno   number(2,0),   
  constraint pk_emp primary key (empno),   
  constraint fk_deptno foreign key (deptno) references dept (deptno)   
)
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

