slip21_2: Create an employee class(id,name,deptname,salary). Define a default and 
parameterized constructor. Use ‘this’ keyword to initialize instance variables. Keep a 
count of objects created. Create objects using parameterized constructor and display the 
object count after each object is created. (Use static member and method). Also display 
the contents of each object. 
class Employee 
{ 
 int id; 
 String name,deptname; 
 double sal; 
 static int cnt=0; 
 Employee() 
 { 
 cnt++; 
 displayCount(); 
 } 
 Employee(int id,String name,String deptname,double sal) 
 { 
 this.id=id; 
 this.name=name; 
 this.deptname=deptname; 
 this.sal=sal; 
 cnt++; 
 displayCount(); 
 } 
 public static void displayCount() 
 { 
 System.out.println("Total Objects created "+cnt); 
 } 
 public void displayData() 
 { 
 System.out.println(this.id+"\t\t"+this.name+"\t\t\t"+this.deptname+"\t\t"+this.
sal); 
 
 } 
 public static void main(String args[]) 
 { 
 Employee e1=new Employee(101,"Maithili","HR",120020.20); 
 
 Employee e2=new Employee(102,"Soham","IT",140020.20); 
 Employee e3=new Employee(104,"Akshay","Accounts",100020.20); 
 System.out.println("EID\t\tName\t\t\tDepartment\t\tSalary"); 
 e1.displayData(); 
 e2.displayData(); 
 e3.displayData(); 
 } 
} 
Slip22_1: Write a program to create an abstract class named Shape that contains 
two integers and an empty method named printArea(). Provide three classes 
named Rectangle, Triangle and Circle such that each one of the classes 
extends the class Shape. Each one of the classes contain only the method 
printArea() that prints the area of the given shape. (use method overriding).
import java.util.*; 
abstract class Shape 
{ int n1,n2; 
 public abstract void printArea(); 
 } 
class Rectangle extends Shape 
{ 
 Rectangle(int a,int b) 
 { 
 n1=a; 
 n2=b; 
 } 
 public void printArea() 
 { 
 float area; 
 area=n1*n2; 
 System.out.println("area of rectangle="+area); 
 MOBILE: 9730381255 | WWW.NRCLASSESPUNE.COM | WWW.BCSBCA.COM
 } 
} 
class Triangle extends Shape 
{ 
 Triangle(int a,int b) 
 { 
 n1=a; 
 n2=b; 
 } 
 public void printArea() 
 { 
 float area; 
 area=(n1*n2)/2; 
 System.out.println("area of triangle="+area); 
 } 
} 
class Circle extends Shape 
{ 
 Circle(int a) 
 { 
 n1=a; 
 } 
 public void printArea() 
 { 
 System.out.println("area of circle="+3.142*n1*n1); 
 } 
} 
class Area 
{ 
 public static void main(String args[]) 
 { 
 Scanner sc=new Scanner(System.in); 
 System.out.println("enter 2 values"); 
 int n1=sc.nextInt(); 
 int n2=sc.nextInt(); 
 Rectangle ob=new Rectangle(n1,n2); 
 
 ob.printArea(); 
 Triangle tr=new Triangle(n1,n2); 
 tr.printArea(); 
 Circle cr=new Circle(n1); 
 cr.printArea(); 
 } 
}
