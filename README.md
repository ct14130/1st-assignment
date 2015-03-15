#include <stdio.h>
#include <string.h>

//Timoleon Theofanellis ct14130
//Paraskevi 

int main()
{
	int day, month, year;
	int sum, d, result;
	int a,b1,b2,b3,c1;
	char imera[10];
	
	printf("Dose imerominia:");
	scanf("%d/%d/%d",&day,&month,&year);
	if (month<=2)
		d=0;
	else if (year%4==0) 
		d=-1;
	else 
		d=-2;
	printf("d=%d\n", d);
	a=(365*(year-1)); printf("a=%d\n",a);
	b1=(year-1)/4; printf("b1=%d\n",b1);
	b2=	-(year-1)/100; printf("b2=%d\n",b2);
	b3=(year-1)/400; printf("b3=%d\n",b3);
	c1=(367*month-362)/12; printf("c1=%d\n",c1);
	sum=a+b1+b2+b3+c1+d+day;
	printf("sum=%d\n",sum);
	result=sum%7;
	printf("day =%d\n", result);
	switch(result)
	{
		case 0:
			imera="ÊõñéáêÞ  "; /*https://www.eskimo.com/~scs/cclass/notes/sx8.html*/
			break;
		case 1:
			imera="ÄåõôÝñá  ";
			break;
		case 2:
			imera="Ôñßôç    ";
			break;
		case 3:
			imera="ÔåôÜñôç  ";
			break;
		case 4:
			imera="ÐÝìðôç   ";
			break;
		case 5:
			imera="ÐáñáóêåõÞ";
			break; 
		case 6:
			imera="ÓÜââáôï";
			break;
	}
	return 0;
}
