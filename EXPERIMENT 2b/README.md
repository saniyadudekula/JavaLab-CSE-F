#EXPERIMENT 2b
##TITLE 2b:) method overloading
```
class Sum{
int Sum(int a , int b){
return a+b;
}
int Sum(int a,int b,int c){
return a+b+c;
}
double Sum (double a,double b){
return a+b;
}
public static void main (String args[]){
Sum S = new Sum();
System.out.println("Sum of 2 integer :"+S.Sum(36,46));
System.out.println("Sum of 3 integer :"+S.Sum(20,36,46));
System.out.println("Sum of 2 real number :"+S.Sum(30-465,15-675));
}
}
```
#OUTPUT
[output of overloading](overload.png)
