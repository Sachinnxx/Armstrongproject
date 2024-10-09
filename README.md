public class ArmstrongNumber {

    public static void main(String[] args) {
        int number = 153; // example number to test
        if (isArmstrong(number)) {
            System.out.println(number + " is an Armstrong number.");
        } else {
            System.out.println(number + " is not an Armstrong number.");
        }
    }

    public static boolean isArmstrong(int number) {
        int originalNumber = number;
        int result = 0;
        int numberOfDigits = String.valueOf(number).length();

        while (number != 0) {
            int remainder = number % 10;
            result += Math.pow(remainder, numberOfDigits);
            number /= 10;
        }

        return result == originalNumber;
    }
}
