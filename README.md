# Ex04-Constructor
## Aim:
 To write a C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor.
 
 ## Algorithm:
 ### Step1: 
Start
### Step2:
Create a class and a constructor
### Step3:
Get name, designation, noofexperience, basic salary and insurance amount from the User.
### Step4:
call salary method in constructor to calculate salary.
### Step5:
call display method to display the output.
### Step6:
stop
 ## Program:
 ```c#
using System;
class Employee
{
    string name,designation;
    int experience,basicsalary,insurance;
    double hra,ta,salary1;
    public Employee(string name,string designation,int experience,int basicsalary,int insurance)
    {
        this.name=name;
        this.designation=designation;
        this.experience=experience;
        this.basicsalary=basicsalary;
        this.insurance=insurance;
    }
    public void salary()
    {
        hra = 0.2*this.basicsalary;
        ta = 0.1*this.basicsalary;
        salary1 = hra+ta+this.basicsalary-this.insurance;
    }
    public void display()
    {
        Console.WriteLine("name of employee is {0} having {1} of experience ,working as {2}",this.name,this.experience,this.designation);
        Console.WriteLine("receives {0} of salary",salary1);
    }
    public static void Main(string[] args)
    {
        Employee emp1 = new Employee("Hari","Tester",10,30000,1000);
        emp1.salary();
        emp1.display();
        Employee emp2 = new Employee("Latha","Developer",5,25000,1000);
        emp2.salary();
        emp2.display();
    }
}
 ```
 ## Output:
 ![image](https://github.com/veerapallijanith/Ex04-Constructor/blob/main/exp3.png)

 ## Result:
 Thus C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor is executed successfully.
