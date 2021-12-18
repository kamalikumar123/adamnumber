# adamnumber
import java.util.Scanner;

public class AdamNum {

	static int revDigit(int num) {
		int rev = 0;
		while (num > 0) {
			rev = rev * 10 + num % 10;
			num /= 10;
		}
		return rev;
	}

	static int square(int n) {
		return n * n;
	}

	static boolean checkAdam(int num) {
		int a = square(num);
		System.out.println("Number square: " + a);
		int b = square(revDigit(num));
		System.out.println("Reverse Number Square: " + b);

		return (a == revDigit(b));
	}

	public static void main(String[] args) {

		Scanner sc = new Scanner(System.in);
		System.out.println("Enter the Number: ");
		int n = sc.nextInt();
		if (checkAdam(n)) {
			System.out.println("Adam Number! ");
		} else {
			System.out.println("Not a Adam Number! ");
		}
		sc.close();
	}
}
