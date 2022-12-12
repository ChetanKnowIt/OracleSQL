1. To list all records with sal > 2000 and comm>200

            select * from emp where sal>2000;

            select * from emp where comm>200; 

2. To list all record with job=’Clerk’ or sal>2000
      
            select * from emp where job='Clerk' or sal>2000;

3. To list all employees with sal>1250 and <2850
      
         select * from emp where sal between 1250 and 2850;



4. Retrieve the details (Name, Salary and dept no) of the emp who are working in department code 20

         select ename, sal, deptno from emp where deptno=20;


5. Display the total salary of all employees . Total salary will be calculated as sal+comm+sal*0.10

         select ename, sal+sal*0.10+nvl(comm, 0) "Total Salary" from emp;


6. Display all employees who have joined after 9th june 81.

         select * from emp where hiredate > (’09-june-81’);


7. Display empno,empname,sal, comm and total salary.Total Salary = comm + sal; 

            select empno, ename, sal, comm, sal+nvl(comm,0) "Total Salary" from emp;


8. Display empname,deptno,dname for all employees.

   
         select emp.ename, emp.deptno, dept.dname from emp, dept where emp.deptno = dept.deptno order by dept.deptno;


9. Display empname,deptno,dname for Smith. 

         select emp.ename, emp.deptno, dept.dname from emp, dept where ename like 'SM%';
