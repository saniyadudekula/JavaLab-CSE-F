#EXPERIMENT 2c
##TITLE 2c:)constructor
```
class student{
String Sname;
int Sage;
double Smarks;
student(String name,int age,double marks){
Sname = name;
Sage = age;
Smarks = marks;
}
void display(){
System.out.println("student name:"+ Sname);
System.out.println("student age:"+ Sage);
System.out.println("student marks:"+Smarks);
}
public static void main(String args[]){
student S = new student("saniya",20,920);
S.display();
}
}
```
#OUTPUT
[output of constructor](constructor.png)
