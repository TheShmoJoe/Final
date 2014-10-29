\\This is the main thing where it creates the window from the Window class.

public class Main {

	public static void main(String[] args) {
		
			Window settings = new Window();
			settings.WindowSettings();
			Sprites background = new Sprites();
			background.loadpics();
				}
}



\\This is the window class that makes the window that I want to put the background in

public class Window extends JFrame{
	
	/**
	 * 
	 */
	private static final long serialVersionUID = 1L;
	public Window() {
		super("Last Daydream");
		setLayout(new FlowLayout());
		new JLabel("This is Shmo");
		
	}
	
	public void WindowSettings(){
		
		Window boss = new Window();
		boss.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		boss.setSize(800,600);
		boss.setVisible(true);
		boss.setResizable(true);
		
		
		
	}
	
}


\\This is the class that loads the image and calls the repaint method


public class Sprites extends JPanel {
	 
	/**
	 * 
	 */
	private static final long serialVersionUID = 1L;
	private Image bg;
	private boolean loaded = false;
	
	public void loadpics(){
		
		bg = new ImageIcon("C:\\Users\\Joe\\Videos\\Lynda.com - Java Essential Training (Dec. 2011)\\Exercise Files\\03_GettingStarted\\ExploreEclipse\\src\\Images\\background.jpg").getImage();
		loaded = true;
		repaint();
	}
	
	public void paintComponent(Graphics g){
		if(loaded){
			g.drawImage(bg,0,0,null);
		}
	}
}

