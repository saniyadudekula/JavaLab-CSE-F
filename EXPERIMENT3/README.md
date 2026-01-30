# EXPERIMENT3A
## TITLE:)CONSTRUCTOR 
```
 class student {
int id;
String name;
int age;
//default constructor
student() {
id = 0;
name = "not asigned";
age = 0;
}
//constructor with two parameters
student(int i, String n) {
id = i;
name = n;
age = 0;
}
//constructor with three parameters
student(int i, String n, int a) {
id = i;
name = n;
age = a;
}
void display() {
System.out.println(id + " " + name + " " + age);
}
}
 class Main {
public static void main(String[] args)
{
student s1 = new student();
student s2 = new student(555, "saniya");
student s3 = new student(666, "ayesha", 19);
s1.display();
s2.display();
s3.display();
}
}
```
# output
<img width="372" height="218" alt="3a output" src="https://github.com/user-attachments/assets/b3b3a1cf-5dff-4c70-bd07-928087efd301" />
# EXPERIMENT3B
## TITTLE:)BINARY SEARCH MECHANISM
```
import java.util.Scanner;
class BinarySearch {
	int list[];
	int key;
	int size;
	BinarySearch(int size) {
		list= new int[size];
		key = -1;
		this.size=size;
 	}
 	void setList() {
			Scanner sc = new Scanner(System.in);
			System.out.println("Enter the list items in Ascending Order.");
			for( int i = 0; i < size; i++) {
					System.out.print("Enter the value of " + (i + 1) + " item: ");
				list[i] = sc.nextInt();
			}
			sc.close();
}
	void getList() {
		for(int i = 0; i < size; i++) 
		System.out.print(list[i] + ".");
    System.out.println("\b\b.");
}
	int binarySearch(int key) {
		int low = 0; int high = list.length; int mid = 0;
		while(low < high) {
			mid = (low + high) / 2;
			if(list[mid] == key) {
				break;
}
elseif(list[mid]<key){
low=mid+1;
}
else
high=mid+1;
}
return list[mid]==key?mid:-1;
}
}
```
# output
<img width="415" height="208" alt="3b output" src="https://github.com/user-attachments/assets/445e082c-9ce7-4249-a77a-a8eceb8e415d" />
# EXPERIMENT3C
## TITTLE:)BUBBLE SORT
```
import java.util.Scanner;
   class BubbleSort {
	void bubbleSort(int arr[]) {
		int n = arr.length;
		int temp = 0;
		for(int i=0 ; i < n-1 ; i++) {
			for(int j=0; j<n-i-1; j++) {
				if(arr[j] > arr[j+1]) {
	temp = arr[j+1];
					arr[j+1] = arr[j];
					arr[j] = temp;
	}
			}
		}

	}

}
class Main {
		public static void main(String args[]) {
		System.out.print("Enter the size of array: ");
		Scanner sc = new Scanner(System.in);
		int size = sc.nextInt();
		int integer[] = new int[size];
		for(int i = 0; i < size; i++) {
			System.out.print("Enter the value of integer at index " + (i+1) + ":"); 
			integer[i] = sc.nextInt();
		}
		BubbleSort bs = new BubbleSort();
		bs.bubbleSort(integer);
		System.out.print("The Sorted integer: ");
		for(int i = 0; i < size; i++)
		System.out.print(integer[i] + ", ");
		System.out.println("\b\b.");
	}
}
```
# OUTPUT
<img width="719" height="225" alt="3c output" src="https://github.com/user-attachments/assets/32240553-956d-4248-9684-805345695840" />
