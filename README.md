# processing-learning
// Sets the screen to be 640 pixels wide and 360 pixels high
size(640, 360);
// Set the background to black and turn off the fill color
background(0);//black
noFill();

stroke(255);//white
point(width * 0.5, height * 0.5);
point(width * 0.5, height * 0.25);
//(0,0) is the top-left corner,bottom right corner is (width-1,height-1)

stroke(0, 153, 255);
line(0, height*0.33, width, height*0.33);


#2
int y = 100;
// The statements in the setup() function 
// execute once when the program begins
void setup() {
  size(640, 360);  // Size must be the first statement
  stroke(255);     // Set line drawing color to white
  frameRate(30);
}
// The statements in draw() are executed until the 
// program is stopped. Each statement is executed in 
// sequence and after the last line is read, the first 
// line is executed again.
void draw() { 
  background(0);   // Clear the screen with a black background
  y = y - 1; 
  if (y < 0) { 
    y = height; 
  } 
  line(0, y, width, y);  
}


#no loop
#The noLoop() function causes draw() to only execute once. 
#Without calling noLoop(), the code inside draw() is run continually.
void setup() 
{
  size(640, 360);  // Size should be the first statement
  stroke(255);     // Set line drawing color to white
 //noLoop();
  
 #Redraw
The redraw() function makes draw() execute once. In this example, draw() is executed once every time the mouse is clicked.
void mousePressed() {
  redraw();
}
