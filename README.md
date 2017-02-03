# repoexample
#include<stdio.h>
#include<math.h>

int Primero(int n)
{
	//1 no primero
	if (n==1)
		return 0;
	//2 primero
	if (n==2)
		return 1;
	for (int i=2;i<=sqrt(n);i++)
	{
		if(n%i==0)
			return 0;
	}
	return 1;
}

void NbrePrimero(){
	for (int i=500;i<1401;i++){
 		if(Primero(i)){
  			printf("%d\n",i);
		}
	}
}


int main(void)
{
	int nombre;
	printf("%s\n","Da un nombre\n");
	scanf("%d",&nombre);
	if(Primero(nombre)){
 	printf("%s\n","El numero es Primero");
 	}
 	else
		{printf("%s\n","El numero no es Primero");}

	
	//Nombre primero entre 500 y 1400
	printf("Los numeros primeros entre 500 y 1400 son\n");
	NbrePrimero();
	return 0;
}
