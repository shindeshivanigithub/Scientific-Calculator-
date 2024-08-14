# include <iostream>
 # include <cmath>
 using namespace std;
 
void sum(float a,float b,float &c); void subt(float a,float b,float &c); void mult(float a,float b,float &c); void div(float a,float b,float &c);
 void mod(int d,int e,int &f );void pow(int d,int e,int &f );void sqrt(float a,float &b);
 
 int main()
{ do{
 	char o; float a,b,c;
 	int d,e,f;
 	cout<<"\t**********Calculator**********\n";
 	cout<<"\n\t1. To permorm addition press +:\n"<<"\t2. To perform subtraction press -:\n"<<"\t3. To perform multiplication press *:\n";
 	cout<<"\t4. To perform division press /:\n"<<"\t5. To calculate modulo press %:\n"<<"\t6. To calculate power press ^\n"<<"\t7. To calculate matrix addition press a:\n";
 	cout<<"\t8. To calculate square root press s:\n"<<"\t9. To calculate factorial press !:\n"<<"\t10.To calculate cos@ press 1:\n";
 	cout<<"\t11.To calculate sin@ press 2:\n"<<"\t12.To calculate tan@ press 3:\n";
	 cin>>o;
 	
 	switch (o) {
 		
		 case '+': {
		 
 	cout<<"Enter 1st numuber";cin>>a;
 	cout<<"Enter 2nd number";cin>>b;
 	  sum(a,b,c);
 	  cout<<c;
              	break;}
	 
	 
 	      case  '-': {
 	 	cout<<"Enter 1st numuber";cin>>a;
 	cout<<"Enter 2nd number";cin>>b;
 	subt(a,b,c);
 	cout<<c;
	  	break;}
	  case '*':  {
 	 	cout<<"Enter 1st numuber";cin>>a;
 	cout<<"Enter 2nd number";cin>>b;
 	mult(a,b,c);
 	cout<<c;
	  	break;}
	  case '/':  {
 	 	cout<<"Enter 1st numuber";cin>>a;
 	cout<<"Enter 2nd number";cin>>b;
 	div(a,b,c);
 	cout<<c;
	  	break;}
	  case '%':  {
 	 	cout<<"Enter 1st numuber";cin>>d;
 	cout<<"Enter 2nd number";cin>>e;
 	mod(d,e,f);
 	cout<<f;
	  	break;}
	  case '^':  {
	  	cout<<"Enter the numuber whose poewer you wanna calculate ";cin>>d;
 	cout<<d<<"^";cin>>e;
 	pow(d,e,f);
 	cout<<f;
	  	break;}
	 case 'a' :{ int r, c, a[r][c], b[r][c], sum[r][c], i, j;

    cout << "Enter number of rows (between 1 and 100): ";
    cin >> r;

    cout << "Enter number of columns (between 1 and 100): ";
    cin >> c;

    cout << endl << "Enter elements of 1st matrix: " << endl;

    for(i = 0; i < r; ++i)
       for(j = 0; j < c; ++j)
       {
           cout << "Enter element a" << i + 1 << j + 1 << " : ";
           cin >> a[i][j];
       }

    cout << endl << "Enter elements of 2nd matrix: " << endl;
    for(i = 0; i < r; ++i)
       for(j = 0; j < c; ++j)
       {
           cout << "Enter element b" << i + 1 << j + 1 << " : ";
           cin >> b[i][j];
       }

    for(i = 0; i < r; ++i)
        for(j = 0; j < c; ++j)
            sum[i][j] = a[i][j] + b[i][j];

    cout << endl << "Sum of two matrix is: " << endl;
    for(i = 0; i < r; ++i)
        for(j = 0; j < c; ++j)
        {
            cout << sum[i][j] << "  ";
            if(j == c - 1)
                cout << endl;
        }

    return 0;
}     case 's':{	cout<<"Enter the numuber whose square root you wanna calculate ";cin>>a;
 	cout<<a<<"sqrt =";
 	sqrt(a,b);
 	cout<<b;}
	 	
		break;
	 case '!':{	cout<<"Enter the numuber whose factorial you wanna calculate ";cin>>a;
               int n=1;
		   for (int i=1;i<=a;++i){
           	n*=i;
		   }
		   cout<<a<<"! ="<<n;
		   
			break;
		}
	case '1':{ cout<<"Enter the value to calculate cos@ in radian";cin>>a; b=cos(a);cout<<b;
		break;
	}	
	case '2':{ cout<<"Enter the value to calculate sin@ in radian";cin>>a; b=sin(a);cout<<b;
		break;
	}
	case '3':{ cout<<"Enter the value to calculate tan@ in radian";cin>>a; b=tan(a);cout<<b;
		break;
	}		
		default: cout<<"\t\t*****Invalid choice*****\n";
	 }
        
 
   
 
 } while(true);}
 void sum(float a,float b,float &c) { c= a+b; 
 }
 void subt(float a,float b,float &c) { c= a-b;
 }
 void mult(float a,float b,float &c) { c= a*b; 
 }
 void div(float a,float b,float &c) { c= a/b; 
 }
 void mod(int d,int e,int &f) { f= d%e; 
 }
 void pow(int d,int e,int &f ){f= pow(d,e);
 }
  void sqrt(float a,float &b){b= sqrt(a);
 }
