<矩形类>
/**
文件：GeometricObject1.java
功能：父类
*/
public class GeometricObject1 {
	  private String color = "white";
	  private boolean filled;
	  private java.util.Date dateCreated;
	  
	  /** Construct a default geometric object */
	  public GeometricObject1() {
	    dateCreated = new java.util.Date();
	  }

	  /** Construct a geometric object with the specified color 
	    *  and filled value */
	  public GeometricObject1(String Color, boolean filled) {
	    dateCreated = new java.util.Date();
	    this.color = color;
	    this.filled = filled;
	  }

	  /** Return color */
	  public String getColor() {
	    return color;
	  }

	  /** Set a new color */
	  public void setColor(String color) {
	    this.color = color;
	  }

	  /** Return filled. Since filled is boolean, 
	     its get method is named isFilled */
	  public boolean isFilled() {
	    return filled;
	  }

	  /** Set a new filled */
	  public void setFilled(boolean filled) {
	    this.filled = filled;
	  }
	  
	  /** Get dateCreated */
	  public java.util.Date getDateCreated() {
	    return dateCreated;
	  }
	  
	  /** Return a string representation of this object */
	  public String toString() {
	    return "created on " + dateCreated + "\ncolor: " + color + 
	      " and filled: " + filled;
	  }
	}


/**
文件：Rectangle1.java
功能：子类
*/
public class Rectangle1 extends GeometricObject1 {
	  private double width＝１;
	  private double height＝１;

	  public Rectangle1() {
	  }

	  public Rectangle1(double width, double height) {
	    this.width = width;
	    this.height = height;
	  }

	  public Rectangle1(double width, double height, String color, 
	      boolean filled) {
	    this.width = width;
	    this.height = height;
	    setColor(color);
	    setFilled(filled);
	  }

	  /** Return width */
	  public double getWidth() {
	    return width;
	  }

	  /** Set a new width */
	  public void setWidth(double width) {
	    this.width = width;
	  }

	  /** Return height */
	  public double getHeight() {
	    return height;
	  }

	  /** Set a new height */
	  public void setHeight(double height) {
	    this.height = height;
	  }

	  /** Return area */
	  public double getArea() {
	    return width * height;
	  }

	  /** Return perimeter */
	  public double getPerimeter() {
	    return 2 * (width + height);
	  }
	}


/**
文件：TestRectangle.java
功能：测试类
*/
public class TestRectangle {
	  public static void main(String[] args) {
	   

	    Rectangle1 rectangle1 = new Rectangle1(4, 40);
	    System.out.println("\nA rectangle " + rectangle1.toString());
	    System.out.println("The area is " + rectangle1.getArea());
	    System.out.println("The perimeter is " +
	      rectangle1.getPerimeter());
	    
	    Rectangle1 rectangle2 = new Rectangle1(3.5, 35.9);
	    System.out.println("\nA rectangle " + rectangle2.toString());
	    System.out.println("The area is " + rectangle2.getArea());
	    System.out.println("The perimeter is " +
	      rectangle2.getPerimeter());
	  }
	}
