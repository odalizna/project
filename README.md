# project
print("Bienvenido a la página de registros del Personal de Seguridad: Eulen Seguridad. de la Universidad de Ingeniería y Tecnología (UTEC)")
print("Si desea realizar cualquiera de las siguientes acciones, ingrese el número indicado:")
print("Una vez que haya realizado la acción, puede a volver a ingresar el mismo número si desea hacer la misma acción")
print("Acciones relacionadas con el ingreso del personal que labora en la universidad: 1")
print("Acciones relacionadas con el ingreso de visitantes: 2")
print("Acciones relacionadas con la pérdida de objetos: 3")
print("Bienvenido a la página de registros del Personal de Seguridad: Eulen Seguridad. de la Universidad de Ingeniería y Tecnología (UTEC)")
print("Si desea realizar cualquiera de las siguientes acciones, ingrese el número indicado:")
print("Una vez que haya realizado la acción, puede a volver a ingresar el mismo número si desea hacer la misma acción")
print("Acciones relacionadas con el ingreso del personal que labora en la universidad: 1")
print("Acciones relacionadas con el ingreso de visitantes: 2")
print("Acciones relacionadas con la pérdida de objetos: 3")
print("Acciones relacionadas con el ingreso de contratistas: 4")
print("Acciones relacionadas al registro de alumnos sin carnet: 5")
print("Registro de las guías de remisión de los proveedores: 6")
print("Si deseas terminar o cancelar un proceso: 0")
print("Si deseas realizar otra acción: -1")
accion=10
lnombre=[]
lapellido1=[]
lapellido2=[]
larea=[]
lingreso=[]
lsalida=[]
lobservacion=[]

if accion==1:
    accion = int(input("Ingrese el número de la acción a realizar: "))
    print("Para realizar un nuevo registro: 7")
    print("Para realizar una búsqueda: 8")
    print("Para realizar una actualización de datos: 9")
    print("Para borrar un registro: 10")
    acción("Ingrese el nuevo número de acción:")
    if accion==7:
        nombre=str(input("Ingrese el primer nombre: "))
        lnombre.append(nombre)
        
        apellido=str(input("Ingrese el primer apellido: "))
        lapellido.append(apellido)

        apellido2=str(input("Ingrese el segundo apellido: "))
        lapellido2.append(apellido2)

        area=str(input("Ingrese el área al que pertenece: "))
        larea.append(area)

        ingreso=str(input("Ingrese la hora de ingreso (hh:mm): "))
        lingreso.append(ingreso)

        salida=str(input("Ingrese la hora de salida (hh:mm): "))
        lsalida.append(salida)

        observacion=str(input("Ingrese cualquier observación adicional o SO (Sin Observación): "))
        lobservacion.append(observacion)

        accion=int(input("Siguiente acción: "))
    elif acción==8:
        print("Búsqueda por nombre: 1")
        print("Búsqueda por apellido: 2")
        print("Búsqueda por area: 3")
        print("Búsqueda por hora de ingreso: 4")
        eleccion=int(input("Ingrese el tipo de búsqueda: "))
        if eleccion==1:
            busqueda = str(input("Ingrese el nombre que desea buscar: "))
            a=0
            for x in lnombre:
                if x == busqueda:
                    a=lnombre.index(busqueda)
                    print('El nombre completo de la persona es: {} {} {}, pertenece al area de {}, ingresó a las {} horas y salió a las {} horas'.format(lnombre[a],lapellido[a].lapellido2[a],larea[a],lingreso[a],lsalida[a]))
        elif eleccion==2:
            busqueda = str(input("Ingrese el apellido (primer apellido) que desea buscar: "))
            a=0
            for x in lapellido:
                if x == busqueda:
                    a=lapellido.index(busqueda)
                    print('El nombre completo de la persona es: {} {} {}, pertenece al area de {}, ingresó a las {} horas y salió a las {} horas'.format(busqueda,lapellido[a].lapellido2[a],larea[a],lingreso[a],lsalida[a]))

