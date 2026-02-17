# ADDITIONAL EXPERIMENT01
## TITTLE:)SUBSTRING
```
import java.util.Scanner;

class Substring {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the main string: ");
        String mainString = sc.nextLine();

        System.out.print("Enter the substring to insert: ");
        String subString = sc.nextLine();

        System.out.print("Enter the position: ");
        int position = sc.nextInt();

        if (position >= 0 && position <= mainString.length()) {
            String firstPart = mainString.substring(0, position);
            String secondPart = mainString.substring(position);

            String resultString = firstPart + subString + secondPart;
            System.out.println("Resulting string: " + resultString);
        } else {
            System.out.println("Invalid position");
        }
    }
}
```
# output
<img width="292" height="73" alt="1addexp output" src="https://github.com/user-attachments/assets/0ddcc290-e999-4870-97aa-54bb0e2f508e" />


# ADDITIONAL EXPERIMENT02
## TITTLE:)fibonacci
```

```
# output








# ADDITIONAL EXPERIMENT03
## TITTLE:)palindrome or not
```
import java.util.Scanner;
class Palindrome {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a String:");
        String str= sc.nextLine();
        int start = 0;
        int end = str.length() - 1;
        while (start < end) {
            if (str.charAt(start) != str.charAt(end)) {
                System.out.println(str+" is not a palindrome");
                return;
            }

            start++;
            end--;
        }
        System.out.println(str+" is a palindrome");
    }
}
```
# output
<img width="336" height="52" alt="3addexp output" src="https://github.com/user-attachments/assets/f8e0c6cf-cb8a-4318-a470-4adc4ed81834" />






# ADDITIONAL EXPERIMENT04
## TITTLE:)PERFECT NUMBER OR NOT
```
import java.util.Scanner;
class PerfectNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int num = sc.nextInt();
        int sum = 0;
        for (int i = 1; i < num; i++) {
            if (num % i == 0) {
                sum += i;
            }
        }
 if (sum == num)
            System.out.println(num + "num is a perfect number.");
        else
            System.out.println(num + "num is not a perfect number.");
    }
}
```
# output
<img width="238" height="53" alt="4addexp output" src="https://github.com/user-attachments/assets/010f3380-cde9-4b59-b3e7-085953ad749a" />

