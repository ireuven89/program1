# program1
the first code uploaded to Github by me

package ImageEditing;
public class BasicEditor {
	
	public static void main (String[] args){
		String filename = args[0];
		String function = args[1];
		StdIn.setInput(filename);
		int [][][] pic = ImageEditing.read(filename);
		
		//checks the char value of the second argument and send pic to the
		// right function(fllips verically or horizntaly or turn to greyscale pic)
		if(function.charAt(1) == 'h'){ 
			pic = ImageEditing.FlipHorizontally(pic);
		}
		else if(function.charAt(1) == 'v'){
			pic = ImageEditing.FlipVertically(pic);
		}
		else if(function.charAt(0) == 'g'){
			pic = ImageEditing.greyscale(pic);
		}
		ImageEditing.show(pic);

		
	}
	
}
