It states that subclass should be substitutable for their base class.

suppose we have Class A and Class B as A:B so all the method of A can be access by object of B without give any weird result from that method 

example 
Rectangle{
	width,height
	Rectangle(width height){
		this.width = width;
		this.height=height;
	}
	getheight
	setheight

	getArea(){
	return width*height
	}
}

Square : Rectangle {
width
Square(width){
this.width=width;
}
get 
set

}

main(){
square s(x);
s.getArea();//this will create problem for us a
}