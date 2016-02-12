# Notes

## createWindow
    void createWindow(JFrame frame, int frameHeight, int frameWidth, int positionX, int positionY) {
      frame.setDefaultCloseOperation(WindowConstants.DISPOSE_ON_CLOSE);
      frame.setSize(frameWidth, frameHeight);
      Dimension d = Toolkit.getDefaultToolkit().getScreenSize();
      int x = (d.width - frame.getSize().width) / 2;
      int y = (d.height - frame.getSize().height) / 2;
      framesetLocation(x, y);
      frame.setResizable(false);
      frame.getContentPane().setLayout(null);
    }

## saveText
    public static void saveText(String str, String dateiname) {
      
      try {
          
        byte[] source = str.getBytes();
        FileOutputStream fos = new FileOutputStream(dateiname);
        fos.write(source);
         
      } catch (IOException exc) {
         
        exc.printStackTrace();
          
      }
      
    } 

