public void Button_Click(Object Sender, EventArgs e){
	//Do something when a button is clicked
}

private void InitializeComponent (){
 //Create a button
 Button button = new Button();
 button.Click+=Button_Click;
 //Add Button to the form
 this.Controls.Add(button);
} 