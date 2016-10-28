# RomanToInteger
import java.util.Scanner;
public class RomanToInteger {

	@SuppressWarnings("resource")
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner n=new Scanner(System.in);
System.out.println("Enter a roman number");
String s=n.nextLine();
s=s.toUpperCase();
int count=0;
char[] a=s.toCharArray();
for(int i=0;i<a.length;i++)
{
	switch(a[i])
	{
	case 'I':
		count=count+1;
		break;
	case 'V':
		count=count+5;
		break;
	case 'X':
		count=count+10;
		break;
	case 'L':
		count=count+50;
		break;
	case 'C':
		count=count+100;
		break;
	case 'D':
		count=count+500;
		break;
	case 'M':
		count=count+1000;
		break;
	default:
		break;
		}
}
if(count!=0)
{
if(s.contains("IV") || s.contains("IX"))
	count=count-2;
if(s.contains("XL") || s.contains("XC"))
	count=count-20;
if(s.contains("CD") || s.contains("CM"))
	count=count-200;
System.out.println(count);
}
else
{
	System.out.println("Invalid");
}
	}

}
