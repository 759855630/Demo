# Demo
public class InputDemo {
	public static void main(String[] args) throws IOException {
		InputStream s = System.in;
		
		FileWriter w = new FileWriter("a.txt");
		
		byte[] bys = new byte[1024];
		int len;
		while ((len = s.read(bys)) != -1 ){
			w.write(new String(bys,0,len));
			w.flush();
		}
		
		
		
		
		s.close();
		w.close();
		
		
	}

}
