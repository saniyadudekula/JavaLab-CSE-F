#EXPERIMENT 2
##TITLE 2a:)class mechanism in Java
```
class Rectangle{
 double length;
 double breadth;
double area(){
return (length * breadth);
}
double perimeter(){
return 2 * (length + breadth);
}
public static void main (String args[])
{
Rectangle rect = new Rectangle();
rect.length = 10;
rect.breadth = 5;
double area = rect.area();
double perimeter = rect.perimeter();
System.out.println("area of the rectangle:"+area);
System.out.println("perimeter of the rectangle:"+perimeter);
}
}
```
#OUTPUT
[output of mechanism](mechanism.png)


