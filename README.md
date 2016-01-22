# TODOList

myself TODO list
* NASA World Wind
* https://support.google.com/webdesigner#topic=
* http://www.linuxstory.org/
* elementary OS
* http://www.freebuf.com/tools/82993.html
* http://www.acfun.tv/v/ac2456630
* Iamasoldier6 - 博客园 - http://www.cnblogs.com/Iamasoldier6/
* 微信公共号平台
* http://share.weiyun.com/28ed5b53cdc8580ebc832cad0946851d#root
* http://ms.csdn.net/share/91881676B450BE5BC9DDC05FFA49575C_1_IPHONE_APP


public class Main {
	public static void main(String[] args) {

		java.util.Scanner in = new java.util.Scanner(System.in);

		Clock clock = new Clock(in.nextInt(), in.nextInt(), in.nextInt());

		clock.tick();

		System.out.println(clock);

		in.close();

	}

}
class Display {
private int value ;
private int limit ;
 public Display(int limit){
	 this.limit = limit;
 }
 public void setvalue(int value){
	 this.value = value;
 }
 
 public void increase(){
	 value ++;
	 if(value == limit){
		 value = 0;
	 }
 }
 public int getvalue(){
	 return value;
 }
	
    
    }


class Clock {
private Display hour = new Display(24);
private Display minute = new Display(60);
private Display second = new Display(60);
public Clock(int h, int m, int s){
	 hour.setvalue(h);
	 minute.setvalue(m);
	 second.setvalue(s);
}   

public String toString(){
	
    return String.format("%02d:%02d:%02d\n",hour.getvalue(),minute.getvalue(),second.getvalue()); 
	
}
public void tick(){
	   while (true){
	   second.increase();
	   if (second.getvalue() == 0){
		   minute.increase();
		   if (minute.getvalue() == 0){
			   hour.increase();
		   }
	   }
	   }
	   }	


}

