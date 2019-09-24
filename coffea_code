#include <stdio.h>
#include <stdlib.h>

int main()
{
    int option,i,k;
    double ganancia = 0;
    double total_de_ganacias2019[12][32];
    for(i = 0 ; i < 12 ; i++)
    {
        for (k = 0 ; k < 31 ; k++ )
        {
            total_de_ganacias2019[i][k] = 0;
        }
        
    }
    
    //productos
    double Americano = 36.0,Espresso = 38.0,Latte = 45.0,Soda = 18.0,Agua = 18.0;
    
    //nombre del programa en pantalla
    printf("\n");
    printf(".--------. .--------. .--------. .--------. .--------.     .--\n");
    printf("| .------´ | .----. | | .------´ | .------´ | .------´    / . \\\n");
    printf("| |        | |    | | | |___     | |___     | |___       / /_\\ \\\n");
    printf("| |        | |    | | | .--´     | .--´     | .--´      / _____ \\\n");
    printf("| `------. | `----' | | |        | |        | '------. / /     \\ \\\n");
    printf("`--------´ `--------' `-'        `-'        `--------´ `-       `-'");
    //programa
    while(1)
    {
        //menu archivo imprimir
        printf("\n");
        FILE *options;
        options = fopen("options.txt","r");
        char line[1000];
        while (fgets(line, 100, options) != NULL)
        {
            printf("%s", line);
        }
        fclose(options);
        //programa
        
        printf("\nopcion: ");
        scanf("%d",&option);
        
        //Para facturar
        if(option == 1)
        {
            int answer2,answer3 = 0;
            int tip10 = 0,tip15 = 0,tip20 = 0,tip25 = 0;
            double amount = 0,cantidadrecibida;
            printf("\n");
            printf(".---------------------------------------.\n");
            printf("|\t\t\t\t\t\t\t\t\t\t|\n");
            printf("|\t\t\t - PRODUCTOS -\t\t\t\t|\n");
            printf("|\t\t\t\t\t\t\t\t\t\t|\n");
            printf("| [1] Americano\t\t\t[4] Soda\t\t|\n");
            printf("| [2] Espresso\t\t\t[5] Agua\t\t|\n");
            printf("| [3] Latte\t\t\t\t\t\t\t\t|\n");
            printf("|\t\t\t\t\t\t\t\t\t\t|\n");
            printf("'---------------------------------------'\n\n");
            
            
            while(1)
            {
                int answer,cantidad;
                printf("Producto: ");
                scanf("%d",&answer);
                
                switch(answer)
                {
                    case 1:
                        printf("Cantidad de americanos: ");
                        scanf("%d",&cantidad);
                        amount += (Americano * cantidad);
                        break;
                    case 2:
                        printf("Cantidad de Espresso: ");
                        scanf("%d",&cantidad);
                        amount += (Espresso * cantidad);
                        break;
                    case 3:
                        printf("Cantidad de Latte: ");
                        scanf("%d",&cantidad);
                        amount += (Latte * cantidad);
                        break;
                    case 4:
                        printf("Cantidad de Soda: ");
                        scanf("%d",&cantidad);
                        amount += (Soda * cantidad);
                        break;
                    case 5:
                        printf("Cantidad de Agua: ");
                        scanf("%d",&cantidad);
                        amount += (Agua * cantidad);
                        break;
                }
                printf("\n");
                printf(".---------------------------------------.\n");
                printf("|\t\t\t\t\t\t\t\t\t\t|\n");
                printf("|\t\t\t - CUENTA -\t\t\t\t\t|\n");
                printf("|\t\t\tTotal: %.2f\t\t\t\t|\n",amount);
                printf("|\t\t¿Agregar otro producto? \t\t|\n");
                printf("|\t\t\t\t\t\t\t\t\t\t|\n");
                printf("|\t\t [0] No\t\t[1] Si\t\t\t\t|\n");
                printf("|\t\t\t\t\t\t\t\t\t\t|\n");
                printf("'---------------------------------------'\n\n");
                
                printf("Respuesta: ");
                scanf("%d",&answer);
                if(answer == 0)
                {
                    break;
                }
            }
            printf("\n");
            printf(".---------------------------------------.\n");
            printf("|\t\t\t\t\t\t\t\t\t\t|\n");
            printf("|\t\t\t¿Agregar propina?\t\t\t|\n");
            printf("|\t\t\t\t\t\t\t\t\t\t|\n");
            printf("|\t\t\t[0] No\t\t[1] Si\t\t\t|\n");
            printf("|\t\t\t\t\t\t\t\t\t\t|\n");
            printf("'---------------------------------------'\n\n");
            printf("Respuesta: ");
            scanf("%d",&answer2);
            
            if(answer2 == 1)
            {
                printf("\n");
                printf(".---------------------------------------.\n");
                printf("|\t\t\t\t\t\t\t\t\t\t|\n");
                printf("|\t\t\t¿Que porcentaje?\t\t\t|\n");
                printf("|\t\t\t\t\t\t\t\t\t\t|\n");
                printf("|\t\t\t[1] 10%%\t\t[3] 20%%\t\t\t|\n|\t\t\t\t\t\t\t\t\t\t|\n|\t\t\t[2] 20%%\t\t[4] 25%%\t\t\t|\n");
                printf("|\t\t\t\t\t\t\t\t\t\t|\n");
                printf("'---------------------------------------'\n\n");
                printf("Respuesta: ");
                scanf("%d",&answer3);
                //variables de propinas
                
                tip10 = amount * 0.10;
                tip15 = amount * 0.15;
                tip20 = amount * 0.20;
                tip25 = amount * 0.25;
                
                switch(answer3)
                {
                    case 1:
                        amount = (tip10) + amount;
                        break;
                    case 2:
                        amount = (tip15) + amount;
                        break;
                    case 3:
                        amount = (tip20) + amount;
                        break;
                    case 4:
                        amount = (tip25) + amount;
                        break;
                        
                }
            }
            printf("Total: %.2f\n",amount);
            
            printf("Cantidad recibida: ");
            scanf("%lf",&cantidadrecibida);
            printf("El cambio: %.2f\n",cantidadrecibida-amount);
            
            switch(answer3)
            {
                case 1:
                    amount = amount - (tip10);
                    break;
                case 2:
                    amount = amount - (tip15);
                    break;
                case 3:
                    amount = amount - (tip20);
                    break;
                case 4:
                    amount = amount - (tip25);
                    break;
                    
            }
            ganancia += amount;
            amount = 0;
            
        }
        
        
        if(option == 2) //la funcion dos nos permite ver las ganancias del mes
        {
            int i,k,respuesta;
            double monthly = 0,year = 0;
            
            for(i = 0 ; i < 12 ; i++)
            {
                for (k = 0 ; k < 32 ; k++ )
                {
                    year += total_de_ganacias2019[i][k];
                }
                
            }
            
            printf("Elige un mes para mostrar las ganancias: ");
            //imprimir meses
            scanf("%d",&respuesta);
            
            
            switch(respuesta)
            {
                case 1:
                    for (k = 0 ; k < 32 ; k++ )
                    {
                        monthly += total_de_ganacias2019[0][k];
                    }
                    printf("-GANANCIAS-\n");
                    printf("Mensual:%.2f\n",monthly);
                    printf("Anual: %.2f\n",year);
                    monthly = 0;
                    break;
                case 2:
                    for (k = 0 ; k < 32 ; k++ )
                    {
                        monthly += total_de_ganacias2019[1][k];
                    }
                    printf("-GANANCIAS-\n");
                    printf("Mensual:%.2f\n",monthly);
                    printf("Anual: %.2f\n",year);
                    monthly = 0;
                    break;
                case 3:
                    for (k = 0 ; k < 32 ; k++ )
                    {
                        monthly += total_de_ganacias2019[2][k];
                    }
                    printf("-GANANCIAS-\n");
                    printf("Mensual:%.2f\n",monthly);
                    printf("Anual: %.2f\n",year);
                    monthly = 0;
                    break;
                case 4:
                    for (k = 0 ; k < 32 ; k++ )
                    {
                        monthly += total_de_ganacias2019[3][k];
                    }
                    printf("-GANANCIAS-\n");
                    printf("Mensual:%.2f\n",monthly);
                    printf("Anual: %.2f\n",year);
                    monthly = 0;
                    break;
                case 5:
                    for (k = 0 ; k < 32 ; k++ )
                    {
                        monthly += total_de_ganacias2019[4][k];
                    }
                    printf("-GANANCIAS-\n");
                    printf("Mensual:%.2f\n",monthly);
                    printf("Anual: %.2f\n",year);
                    monthly = 0;
                    break;
                case 6:
                    for (k = 0 ; k < 32 ; k++ )
                    {
                        monthly += total_de_ganacias2019[5][k];
                    }
                    printf("-GANANCIAS-\n");
                    printf("Mensual:%.2f\n",monthly);
                    printf("Anual: %.2f\n",year);
                    monthly = 0;
                    break;
                case 7:
                    for (k = 0 ; k < 32 ; k++ )
                    {
                        monthly += total_de_ganacias2019[6][k];
                    }
                    printf("-GANANCIAS-\n");
                    printf("Mensual:%.2f\n",monthly);
                    printf("Anual: %.2f\n",year);
                    monthly = 0;
                    break;
                case 8:
                    for (k = 0 ; k < 32 ; k++ )
                    {
                        monthly += total_de_ganacias2019[7][k];
                    }
                    printf("-GANANCIAS-\n");
                    printf("Mensual:%.2f\n",monthly);
                    printf("Anual: %.2f\n",year);
                    monthly = 0;
                    break;
                case 9:
                    for (k = 0 ; k < 32 ; k++ )
                    {
                        monthly += total_de_ganacias2019[8][k];
                    }
                    printf("-GANANCIAS-\n");
                    printf("Mensual:%.2f\n",monthly);
                    printf("Anual: %.2f\n",year);
                    monthly = 0;
                    break;
                case 10:
                    for (k = 0 ; k < 32 ; k++ )
                    {
                        monthly += total_de_ganacias2019[9][k];
                    }
                    printf("-GANANCIAS-\n");
                    printf("Mensual:%.2f\n",monthly);
                    printf("Anual: %.2f\n",year);
                    monthly = 0;
                    break;
                case 11:
                    for (k = 0 ; k < 32 ; k++ )
                    {
                        monthly += total_de_ganacias2019[10][k];
                    }
                    printf("-GANANCIAS-\n");
                    printf("Mensual:%.2f\n",monthly);
                    printf("Anual: %.2f\n",year);
                    monthly = 0;
                    break;
                case 12:
                    for (k = 0 ; k < 32 ; k++ )
                    {
                        monthly += total_de_ganacias2019[11][k];
                    }
                    printf("-GANANCIAS-\n");
                    printf("Mensual:%.2f\n",monthly);
                    printf("Anual: %.2f\n",year);
                    monthly = 0;
                    break;
            }
            
        }
        
        
        
        //para cerrar las ganancias del dia y que se guarden en la variable
        if(option == 3)
        {
            //printf("%1f",ganancia); para comprobar que si se esta guardando
            int month,day;
            printf("para guardar los datos ingresa la fecha (formato en numero: MM,DD) : ");
            scanf("%d,%d",&month,&day);
            while(month < 1 || month > 12 || day < 1 || day > 31)
            {
                printf("Entrada incorrecta\n");
                printf("para guardar los datos ingresa la fecha (formato en numero: MM,DD) : ");
                scanf("%d,%d",&month,&day);
            }
            total_de_ganacias2019[month-1][day-1] = ganancia;
            printf("\nse guardo: %.2f\n",total_de_ganacias2019[month-1][day-1]);
            ganancia = 0;
            
            
        }
        
        if(option == 4)
        {
            while(1){
            int risposta;
            FILE *menu;// estamos declarando una variable de tipo FILE
            // Esta variable almacena la información que nos permite leer a un archivo.
            menu = fopen("menu.txt","r");// la función fopen busca en la misma carpeta que el ejecutable por un archivo
            // "r":  sólo lectura. Si no existe, regresa NULL
            if (menu == NULL) // si es NULL significa que no se pudo abrir el archivo
            {
                puts("No funciono"); // indicamos al usuario del error
                return -1;                                                           // terminamos el programa con código de error.
            }
            char line[1000]; // Este arreglo de caracteres vamos a usarlo para leer cada línea del archivo, una por una.
            while (fgets(line, 100, menu) != NULL) // si el resultado que regrese fgets es NULL, significa que no leyó nada.
            {
                
                printf("%s", line); // lo único que hacemos es imprimir cada línea que vamos leyendo,para leer los artículos de una compra,
                
            }
            fclose(menu);
            printf("\n¿Desea volver al menu principal?\n\n\t\t\t[1] Si\t\t\t\t");
            printf("\n\nRespuesta: ");
            scanf("%d",&risposta);
            while(risposta !=1)
            {
                printf("Entrada incorrecta, presiona [1] para volver al menu principal: ");
                scanf("%d",&risposta);
            }
            if(risposta == 1)
            {
                break;
            }
                return 0;
                
          }
        }
        
    }
    
}
