# Demo
public class InputDemo {
	public static void main(String[] args) throws IOException {
	
		//创建输入流对象
		InputStream s = System.in;
		//创建输出流对象
		FileWriter w = new FileWriter("a.txt");
		
		byte[] bys = new byte[1024];
		int len;//用于存储读到的字节个数
		while ((len = s.read(bys)) != -1 ){
			w.write(new String(bys,0,len));
			w.flush();
		}
		
		
		
		//释放资源
		s.close();
		w.close();
		
		
	}

}
