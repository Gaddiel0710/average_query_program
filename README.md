# average_query_program
## _program to consult the average of assigned subjects_
### used libraries
```python
import os
import time as ti
import msvcrt as ms
```
### average query function
```python
def GZF_promedio(GZF_nombre_materia, GZF_val_examen, GZF_val_tareas, GZF_val_firmas,GZF_pts_examen, GZF_pts_tareas,GZF_pts_firmas):
    salida=0
    while salida ==0:
        GZF_nombre = str(input("Ingrese su nombre: "))
        os.system('cls')
        GZF_examen = float(input("Ingrese la calificacion obtenida en su examen entre: "))
        os.system('cls')
        GZF_tareas = float(input("Ingrese el numero de tareas calificadas entre: "))
        os.system('cls')
        GZF_firmas = float(input("Ingrese numero de practicas o firmas entre: "))
        os.system('cls')
        print("Calculando promedio...")
        ti.sleep(2)
        os.system('cls')
        GZF_calif_examen = (GZF_examen *GZF_val_examen) / GZF_pts_examen
        GZF_calif_tareas = (GZF_tareas * GZF_val_tareas)/GZF_pts_tareas
        GZF_calif_firmas = (GZF_firmas *GZF_val_firmas) / GZF_pts_firmas
        GZF_promedio_final = GZF_calif_examen + GZF_calif_tareas + GZF_calif_firmas
        GZF_promedio_final = round(GZF_promedio_final,1)
        if(GZF_promedio_final > 10):
            os.system('cls')
            print("los valores ingresado no son validos")
            ti.sleep(1.5)
            os.system('cls')
            salida = 1
        else:
            os.system('cls')
            GZF_resultado= "El promedio general de "+GZF_nombre+" en la materia de "+GZF_nombre_materia+" es: "+str(GZF_promedio_final)
            ti.sleep(1)
            print(GZF_resultado)
            print("\n presione una tecla para regresar al menu")
            ms.getch()
            salida = 1
```

### Principal function
``` python
def main():
    bucle =1
    while bucle ==1:
        os.system('cls')
        print("BIENVENIDO A LA CONSULTA DE PROMEDIOS\n")
        #Menu
        print(" ==Menú de materias==")
        ti.sleep(1/4)
        print("1.-Sensores")
        ti.sleep(1/4)
        print("2.-Programación")
        ti.sleep(1/4)
        print("3.-Mecanismos")
        ti.sleep(1/4)
        print("4.-Controladores")
        ti.sleep(1/4)
        print("0.-salir")
        ti.sleep(1/2)
        GZF_materia = int(input("""\nSeleccione la materia que desea promediar
-->  """))
        if GZF_materia == 1:
            os.system('cls')
            GZF_promedio( "Sensores", 4.5, 2.5, 3, 10, 3, 5)
            bucle =1
        elif GZF_materia == 2:
            os.system('cls')
            GZF_promedio("Programación", 3, 5, 2, 10, 3, 5)
            bucle =1
        elif GZF_materia == 3:
            os.system('cls')
            GZF_promedio("Mecanismos", 5.5, 1, 3.5, 10, 3, 6)
            bucle =1
        elif GZF_materia == 4:
            os.system('cls')
            GZF_promedio( "Controladores", 2, 2, 6, 10, 2, 5)
            bucle =1
        elif GZF_materia ==0:
            os.system('cls')
            ti.sleep(1/2)
            print("\n gracias por utilizar nuestro sistema de promedios")
            ti.sleep(1)
            print(" ")
            print("Vuelva pronto ... ;)")
            ti.sleep(1/2)
            bucle =0
        else:
            os.system('cls')
            print("El valor ingresado no es valido")
            ti.sleep(1/2)
            os.system('cls')
            bucle=1
    os.system('cls')

if __name__ == "__main__":
    main()
```
