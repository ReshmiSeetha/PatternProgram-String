# PatternProgram-String
/*
Input : W E L C O M E
Explanation : start with middle letter from first line. Next line two letter from middle . Continue
still you print all letters in last line. Then start with the first letter and continue for the remaining
letters.
output :
            C
          C O
        C O M
      C O M E
    C O M E W
   C O M E W E
 C O M E W E L

*/
import java.util.*;
public class Main
{
    public static void printWord(String res,int len){
        while(len!=0){
		        System.out.print(" ");
		        len--;
		    }
		    System.out.println(res);
    }
	public static void main(String[] args) {
		Scanner s=new Scanner(System.in);
		String Value=s.nextLine();
		int middle=Value.length()/2;
		String res="";
		for(int i=middle;i<Value.length();i++){
		    res+=Value.charAt(i);
		    int len=Value.length()-res.length();
		    printWord(res,len);
		}
		for(int i=0;i<middle;i++){
		    res+=Value.charAt(i);
		    int len=Value.length()-res.length();
		    printWord(res,len);
		}
	}
}

