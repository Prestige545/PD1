import java.awt.Canvas;
import java.awt.Graphics;
import java.awt.Graphics2D;
import java.awt.Shape;
import java.awt.geom.Ellipse2D;
import java.awt.geom.GeneralPath;
import java.awt.geom.Line2D;
import java.awt.geom.Rectangle2D;
import java.awt.geom.RoundRectangle2D;

import javax.swing.JFrame;

public class obiekty extends JFrame {
  Shape shapes[] = new Shape[5];
  public static void main(String args[]) {
    obiekty app = new obiekty();
  }

  public obiekty() {
    add("Center", new MyCanvas());
    shapes[0] = new Line2D.Double(0.0, 0.0, 100.0, 100.0); // rysuje linie
    shapes[1] = new Rectangle2D.Double(50.0, 200.0, 200.0, 200.0); // rysuje kwadrat
    shapes[2] = new Ellipse2D.Double(20.0, 420.0, 300.0, 300.0); // rysuje koło
    GeneralPath path = new GeneralPath(new Line2D.Double(300.0, 100.0, 400.0, 150.0));
    path.append(new Line2D.Double(25.0, 175.0, 300.0, 100.0), true);
    shapes[3] = path; // rysuje trojkat
    setSize(400, 400);
    setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    setVisible(true);
  }

  class MyCanvas extends Canvas {
    public void paint(Graphics graphics) {
      Graphics2D g = (Graphics2D) graphics;
      for (int i = 0; i < shapes.length; ++i) {
        if (shapes[i] != null)
          g.draw(shapes[i]);
      }
    }
  }
}
