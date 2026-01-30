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
<img width="292" height="73" alt="Screenshot 2026-01-23 160918" src="https://github.com/user-attachments/assets/2ba23135-885b-4af0-9f6e-931bc27b6a46" />



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
<img width="336" height="52" alt="Screenshot 2026-01-30 222649" src="https://github.com/user-attachments/assets/0f1f35c4-2d05-44a2-9599-a0e077540c76" />





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
<img width="238" height="53" alt="Screenshot 2026-01-30 223714" src="https://github.com/user-attachments/assets/7ec40960-1145-4087-b197-60ea84333be5" />

