# Palandrome-Recursion
public class palandrome {
	public static void main(String[] args) {
		String s = "KAYAK";
		System.out.println(s + (pal(s) ? " is" : " is not") + " a palindrome.");

	}

	public static boolean pal(String s1) {

		// if the length is one or 0 then it made it past all the check methods
		// and is true
		if (s1.length() < 2) {
			return true;
		}
		// if it still has a length 2 or greater than take the numbers on
		// opposite ends of the string and check to see if they are true or
		// false
		else if (s1.charAt(0) != s1.charAt(s1.length() - 1))
			return false;
		// other wise shorted each side with recursion by eliminating the first
		// and last index's of the string
		else

			return pal(s1.substring(1, s1.length() - 1));

	}
}
