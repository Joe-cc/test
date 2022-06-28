# test
import java.util.ArrayList;
import java.util.Scanner;

// 禮物配對
public class Test1 {

	public static void main(String[] args) {
		Scanner scn = new Scanner(System.in);
		System.out.println("請輸入人數:");
		int num = scn.nextInt();
		ArrayList<String> group = new ArrayList<String>(num);
		System.out.println("請輸入人名:");
		for(int i=0; i<num; i++) {
			String person = scn.next();
			group.add(person);
		}
		for(int i=0;i<num/2;i++) {
			for(int j=0;j<2;j++) {
				int r=(int)(Math.random()*group.size());
				System.out.print(group.get(r)+" ");
				group.remove(r);
			}
			System.out.println();
		}
		scn.close();

	}

}
