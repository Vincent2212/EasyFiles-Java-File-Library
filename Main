// Main class

import java.util.*;
import java.io.*;
// EasyFiles will not format written and read file text for you. That is completely up to you.


public class EasyFiles {
	public String file;
	
	public EasyFiles(String file) {
		this.file = file;
	}


	public String read() {
		try {
			File myFile = new File(this.file);
			Scanner readFile = new Scanner(myFile);
			String contents = "";

			while (readFile.hasNextLine()) {
				contents += readFile.nextLine();
			}

			return contents;
		}
		catch (IOException e) {
			System.out.println("EasyFiles encountered an exception reading this file.");
			e.printStackTrace();
			return null;
		}
	}

	public void write(String WriteContents, boolean appendMode) {
		try {
			if (!appendMode) {
				FileWriter writeFile = new FileWriter(this.file);
				writeFile.write(WriteContents);
		    writeFile.close();
			} else {
			  FileWriter writeFile = new FileWriter(this.file, true);
				writeFile.write(WriteContents);
		    writeFile.close();
			}
		}
		catch (IOException e) {
			System.out.println("EasyFiles encountered an exception writing to this file.");
			e.printStackTrace();
		}
	}


	public void clear() {
		try {
			FileWriter writeFile = new FileWriter(this.file);
			writeFile.write("");
		  writeFile.close();
		}
		catch (IOException e) {
			System.out.println("EasyFiles encountered an exception attempting to clear this file.");
			e.printStackTrace();
		}
	}

  public boolean createFile() {
    try {
      File myFile = new File(this.file);
      if (myFile.exists()) {
        return false;
      }
      myFile.createNewFile();
      return true;
    }
    catch (IOException e) {
      System.out.println("EasyFiles encountered an exception creating this file.");
      e.printStackTrace();
      return false;
    }
  }
}
