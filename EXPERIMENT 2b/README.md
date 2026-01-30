# EXPERIMENT 2b
## TITLE 2b:) method overloading
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
# OUTPUT
<img width="479" height="171" alt="exp2b" src="https://github.com/user-attachments/assets/895c5617-0ab2-4f31-8946-01a4ee988e29" />
