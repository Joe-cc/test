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

import java.util.HashMap;
import java.util.Map;
import java.util.Scanner;

//學生科目和老師配對
public class Test2 {

	public static void main(String[] args) {
		Map<String, String> st = new HashMap<>();
		String [] suject = {"國文","英文","數學","社會","自然"};
		String []  name  = {"李老師","張老師","林老師","王老師","陳老師"};
		for(int i = 0; i < name.length; i++)
			st.put(suject[i],name[i] );
		
		boolean dataFlag = false;
		
		Scanner scn = new Scanner(System.in);
		System.out.print("請輸入科目名稱(國文、英文、數學、社會、自然):");
		while(!dataFlag) {
			String input = scn.nextLine();
			if(st.containsKey(input) == false)
				System.out.println("沒有此科目請重新輸入!!");
			else{
				System.out.println("此科目的老師為:" + st.get(input));
				dataFlag = true;
			}				
		}
		scn.close();
	}
}


[1-日本地酒-水果酒系-202201206更新.pdf](https://github.com/Joe-cc/test/files/10214359/1-.-.-202201206.pdf)
[2-日本地酒-清酒系燒酎系-20221118更新.pdf](https://github.com/Joe-cc/test/files/10214360/2-.-.-20221118.pdf)
[9-贈酒及促銷20221118更新.pdf](https://github.com/Joe-cc/test/files/10214364/9-.20221118.pdf)

