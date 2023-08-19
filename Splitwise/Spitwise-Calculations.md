	In the end if my balance is in + that means I have paid more
	- means I have to pay
	+ paying 
	- sharing 
	
	RoomMate RM Expanses
	
	E1=
	T=1000
	pb=A(500) B(500) 
	sb=A(500) B(250) C(250)
	
	E2=
	T=2000
	pb=C(2000)
	sb=A(1000) B(500) C(500)
	
	
	
	A=?  E1(+pb.A -sb.A)+ E2(0-sb.A)
			0 + (-1000) + 0 + 0 = -1000
	B=?  E1(+pb.B -sb.B)+ E2(0-sb.B)
			250 + (-500) = -250
	C=?  -250 +2000 -500 = 1250
	
	Office Expanses 
	
	E3=
	T=3000
	pb=D(3000)
	sb=B(1000) C(1000) D(1000)
	
	E4=
	T=2000
	pb=B(1000) C(1000)
	sb=B(1000) C(500) D(500)
	
	B=? E3(pb.B-sb.B) + E4(pb.B-sb.B)
		0-1000 + 1000 -1000 = -1000
	
	C=? E3(pb.C-sb.C) + E4(pb.C -sb.C)
		0-1000 + 1000-500 = -500
	
	D=? E3(pb.D-sb.D) + E4(pb.D -sb.D)
		3000 - 1000 + 0 - 500 = 1500
		
	Now to settle this we need some transactions to be done
	Suppose we want to settle roommates 
	A->C 1000
	B->C 250    so that C will receive 1250 and everyones balance will be 0
	
	Sililarly B->D 1000
			  C->D 500 and D <- 1500 
			  
			  
	Minimising transactions
	A +100
	B -200
	C -100
	D +200
	
	Round-Trip Algorithm
	{if n participant -> n-1 transaction}
	because in every transaction 1 person will be settled
	Greedy Algorithm