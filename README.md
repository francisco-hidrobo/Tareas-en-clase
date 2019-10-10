# Tareas-en-clase
/******************************************************************************
Columna2.- Se desea calcular el salario neto semanal de un trabajador en función 
del número de horas trabajadas y la tasa de impuestos:
Las primeras 35 horas de pagan a tarifa normal.
Las horas que pasen de 35 se pagan a 1.5 veces la tarifa normal Las tasas de impuestos son:
1. Losprimeros1000dólaressonlibresdeimpuestos.
2. Lossiguientes500dólarestienenun25%deimpuestos. 3. Losrestantes,un45%deimpuestos.
La tarifa horaria es de 40 dólares
Se desea escribir el SALARIO BRUTO(salario antes de impuesto), TASAS DE IMPUESTOS , 
Y SALARIO NETO(salario después de impuestos).
*******************************************************************************/

#include<stdio.h>
/*definimos constantes*/
#define tarifahoraria 40

/*Se declara la función principal*/
void main()
{
	/*Se declaran las variables*/
	float salarioneto=0, salariobruto,horas,tasaimpuesto=0;
	char nombre[10];
	printf("Ingresar el nombre del trabajador:");
	scanf("%s",nombre);
	printf("Ingresar las horas de trabajo:");
	scanf("%f",&horas);
	/*Ahora debemos conocer los salariosdeterminamos los salarios si las horas trabajadas son menor o igual a 35*/
	if(horas<=35)
	{
	salariobruto=horas*tarifahoraria;
	/*Dependiendo del salario en bruto se determinan los impuestos*/
	    if(salariobruto>1000 && salariobruto<=1500)
    	{
    	tasaimpuesto=salariobruto*0.25;
    	salarioneto=salariobruto-tasaimpuesto;		
    	printf("El trabajador:%s\nSu salario bruto es:%.2f\nLa tasa de impuesto es:%.2f\nEl salario neto es:%.2f",nombre,salariobruto,tasaimpuesto,salarioneto);
	
    	    else if(salariobruto>1500)
    	    tasaimpuesto=salariobruto*0.45;
    	    salarioneto=salariobruto-tasaimpuesto;		
    	    printf("El trabajador:%s\nSu salario bruto es:%.2f\nLa tasa de impuesto es:%.2f\nEl salario neto es:%.2f",nombre,salariobruto,tasaimpuesto,salarioneto);
	
    	    else
	
	    salarioneto=salariobruto;
	printf("El trabajador:%s\nSu salario bruto es:%.2f\nLa tasa de impuesto es:%.2f\nEl salario neto es:%.2f",nombre,salariobruto,tasaimpuesto,salarioneto);
	}
	else
	{
	salariobruto=horas*tarifahoraria*1.5;
	/*Ahora se determina los impuestos a pagar dependiendo del salario bruto*/
	if(salariobruto>1000 && salariobruto<=1500)
	{
	tasaimpuesto=salariobruto*0.25;
	salarioneto=salariobruto-tasaimpuesto;
	printf("El trabajador:%s\nSu salario bruto es:%.2f\nLa tasa de impuesto es:%.2f\nEl salario neto es:%.2f",nombre,salariobruto,tasaimpuesto,salarioneto);
	}
	else if(salariobruto>1500)
	{
	tasaimpuesto=salariobruto*0.45;
	salarioneto=salariobruto-tasaimpuesto;
	printf("El trabajador:%s\nSu salario bruto es:%.2f\nLa tasa de impuesto es:%.2f\nEl salario neto es:%.2f",nombre,salariobruto,tasaimpuesto,salarioneto);
	}
	else
	{
	salarioneto=salariobruto;
	printf("El trabajador:%s\nSu salario bruto es:%.2f\nLa tasa de impuesto es:%.2f\nEl salario neto es:%.2f",nombre,salariobruto,tasaimpuesto,salarioneto);
		}
	}
}
