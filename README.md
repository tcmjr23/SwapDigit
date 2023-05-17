# SwapDigit
This project swaps each pair of digits within a value

Here is sample code of this project:

# public static int swapDigitPairs(int n) {
		int swap = 0;
		int temp1 = 0;
		int temp2 = 0;
		for(int i = 1;n>0;i*=100) {
			temp1 = n%10;
			n/=10;
			if(n==0) {
				if(i==0) {
				swap +=temp1*1;
				}else {
					System.out.println("test"+temp1);
					swap +=(temp1*i);
					temp1 = (temp1*((i*10)));
					System.out.println("after else"+temp1);
				}
			}
			else {
				temp2 = n%10;
				System.out.println("ladder" + temp1);
				temp1 = (temp1*(i*10));
				System.out.println("after temp1 =" + temp1);
				System.out.println("temp2: " + temp2);
				if(i>1) {
					temp2 *= i;
					System.out.println("math.pow result: " + temp2);
				}
				swap += temp1+temp2;
				n/=10;
				System.out.println(temp1 + " + " + temp2 + "   swap: " + swap);
			}
		}
		System.out.println("swap: " + swap);
		return swap;
	}
 This code used mod(%) and /10 to isolate the integer in the ones and tens place which is then stored in a temp value. With the for loop variable i which is multiplied by 100 after every loop, I am able to manipulate the value of certain integers and add them to the return value. This way, each integer is in their newly defined place. This project taught us how to manage variables and manipulate text using loops.   
