print("Bienvenido a la página de registros del Personal de Seguridad: Eulen Seguridad. de la Universidad de Ingeniería y Tecnología (UTEC)")
print("Si desea realizar cualquiera de las siguientes acciones, ingrese el número indicado:")
print("Una vez que haya realizado la acción, puede a volver a ingresar el mismo número si desea hacer la misma acción")
print("Acciones relacionadas con el ingreso del personal que labora en la universidad: 1")
print("Acciones relacionadas con el ingreso de visitantes: 2")
print("Acciones relacionadas con la pérdida de objetos: 3")
print("Acciones relacionadas con el ingreso de contratistas: 4")
print("Registro de alumnos sin carnet: 5")
print("Registro de las guías de remisión de los proveedores: 6")
print("Si deseas realizar otra acción: -1")
lnombre=[]
lapellido=[]
lapellido2=[]
larea=[]
lingreso=[]
lsalida=[]
lobservacion=[]
accion=-1
while accion==-1:
    accion = int(input("Ingrese el número de la acción a realizar: "))
    if accion==1:
        print("Para realizar un nuevo registro: 1")
        print("Para realizar una búsqueda: 2")
        print("Para realizar una actualización de datos: 3")
        print("Para borrar un registro: 4")
        accion=int(input("Ingrese su nuevo número: "))
        if accion==1:
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
            opcion = int(input("Opcion 1: Agregar otro registro. Opción 2: Volver al menú"))
            if opcion == 1:
                pass
            else:
                break
        elif accion==2:
            print("Búsqueda por nombre: 1")
            print("Búsqueda por apellido: 2")
            print("Búsqueda por area: 3")
            print("Búsqueda por hora de ingreso: 4")
            eleccion=int(input("Ingrese el tipo de búsqueda: "))
            def salida (o,n):
                a=0
                for x in n:
                    if x == o:
                        a=n.index(o)
                        return('El nombre completo de la persona es: {} {} {}, que pertenece al area de {}, ingresó a las {} horas y salió a las {} horas'.format(lnombre[a],lapellido[a].lapellido2[a],larea[a],lingreso[a],lsalida[a]))
            while eleccion!=0:
                if eleccion==1:
                    busqueda = str(input("Ingrese el nombre que desea buscar: "))
                    print(salida(busqueda,lnombre))
                elif eleccion==2:
                    busqueda1 = str(input("Ingrese el apellido (primer apellido) que desea buscar: "))
                    print(salida(busqueda1,lapellido))
                elif eleccion==3:
                    busqueda2 = str(input("Ingrese el area de la que desea que aparezca la cantidad y las personas que ingresaron: "))
                    a=0
                    cont=0
                    for x in larea:
                        if x == busqueda2:
                            cont = cont +1
                            a=larea.index(busqueda2)
                            print('La cantidad de personas del área de {}, que ingresaron fueron {}'.format(busqueda,cont))
                            print('El nombre completo de la persona es: {} {} {}, que pertenece al area de {}, ingresó a las {} horas y salió a las {} horas'.format(lnombre[a],lapellido[a].lapellido2[a],larea[a],lingreso[a],lsalida[a]))
                elif eleccion==4:
                    busqueda3 = str(input("Ingrese la hora de ingreso para buscar a la persona por este criterio: "))
                    print(salida(busqueda3,lingreso))
                else:
                    print("Ingrese un valor aceptable")
                    pass
                opcion = int(input("Opción 1: Buscar otro dato. Opción 2: Volver al menú"))
                if opcion == 1:
                    pass
                else:
                    break
        elif accion==3:
            actualizar = str(input("Ingrese el nombre o el primer apellido del registro que quiere actualizar: "))
            for i in lnombre:
                def actualizacion(lista,dato):
                    posicion=0
                    posicion=lista.index(actualizar)
                    lista[posicion]=(dato)
                while actualizar==i:

                    print("¿Qué dato desea actualizar?")
                    print("Nombre: 1")
                    print("Primer apellido: 2")
                    print("Segundo apellido: 3")
                    print("El área: 4")
                    print("La hora de ingreso: 5")
                    print("La hora de salida: 6")
                    datoac=int(input("Ingrese el número de dato a actualizar: "))

                    if datoac==1:
                        nombreac=str(input("Ingrese el nuevo nombre: "))
                        actualizacion(lnombre,nombreac)
                        pass
                    print("Opcion 1: Actualizar otro dato. Opción 2: volver al menu")
                    opcion = int(input())
                    if opcion == 1:
                        pass
                    else:
                        break
                    if datoac==2:
                        apellidoac=str(input("Ingrese el nuevo primer apellido: "))
                        actualizacion(lapellido,apellidoac)
                        pass
                    print("Opcion 1: Actualizar otro dato. Opción 2: volver al menu")
                    opcion = int(input())
                    if opcion == 1:
                        pass
                    else:
                        break
                    if datoac==3:
                        apellido2ac=str(input("Ingrese el nuevo segundo apellido: "))
                        actualizacion(lapellido2,apellido2ac)
                        pass
                    print("Opcion 1: Actualizar otro dato. Opción 2: volver al menu")
                    opcion = int(input())
                    if opcion == 1:
                        pass
                    else:
                        break
                    if datoac==4:
                        ingresoac=str(input("Ingrese la nueva hora de ingreso (hh:mm): "))
                        actualizacion(lingreso,ingresoac)
                        pass
                    print("Opcion 1: Actualizar otro dato. Opción 2: Volver al menú")
                    opcion = int(input())
                    if opcion == 1:
                        pass
                    else:
                        break
                    if datoac==5:
                        salidaac=str(input("Ingrese la nueva hora de salida (hh:mm): "))
                        actualizacion(lsalida,salidaac)
                        pass
                    print("Opcion 1: Actualizar otro dato. Opción 2: volver al menu")
                    opcion = int(input())
                    if opcion == 1:
                        pass
                    else:
                        break
            for j in lapellido:
                while actualizar==i:

                    print("¿Qué dato desea actualizar?")
                    print("Nombre: 1")
                    print("Primer apellido: 2")
                    print("Segundo apellido: 3")
                    print("El área: 4")
                    print("La hora de ingreso: 5")
                    print("La hora de salida: 6")
                    datoac=int(input("Ingrese el número de dato a actualizar: "))

                    if datoac==1:
                        nombreac=str(input("Ingrese el nuevo nombre: "))
                        actualizacion(lnombre,nombreac)
                        pass
                    print("Opcion 1: Actualizar otro dato. Opción 2: volver al menu")
                    opcion = int(input())
                    if opcion == 1:
                        pass
                    else:
                        break
                    if datoac==2:
                        apellidoac=str(input("Ingrese el nuevo primer apellido: "))
                        actualizacion(lapellido,apellidoac)
                        pass
                    print("Opcion 1: Actualizar otro dato. Opción 2: volver al menu")
                    opcion = int(input())
                    if opcion == 1:
                        pass
                    else:
                        break
                    if datoac==3:
                        apellido2ac=str(input("Ingrese el nuevo segundo apellido: "))
                        actualizacion(lapellido2,apellido2ac)
                        pass
                    print("Opcion 1: Actualizar otro dato. Opción 2: volver al menu")
                    opcion = int(input())
                    if opcion == 1:
                        pass
                    else:
                        break
                    if datoac==4:
                        ingresoac=str(input("Ingrese la nueva hora de ingreso (hh:mm): "))
                        actualizacion(lingreso,ingresoac)
                        pass
                    print("Opcion 1: Actualizar otro dato. Opción 2: Volver al menú")
                    opcion = int(input())
                    if opcion == 1:
                        pass
                    else:
                        break
                    if datoac==5:
                        salidaac=str(input("Ingrese la nueva hora de salida (hh:mm): "))
                        actualizacion(lsalida,salidaac)
                        pass
                    print("Opcion 1: Actualizar otro dato. Opción 2: volver al menu")
                    opcion = int(input())
                    if opcion == 1:
                        pass
                    else:
                        break

        elif accion==4:
            borrar = str(input("Ingrese el nombre o el primer apellido del registro que quiere borrar: "))
            def eliminar(lista):
                posicion=0
                posicion=lista.index(borrar)
                lista.pop(posicion)
            for i in lnombre:
                while borrar==i:
                    eliminar(lnombre)
                    eliminar(lapellido)
                    eliminar(larea)
                    eliminar(lingreso)
                    eliminar(lsalida)
                    eliminar(lobservacion)
                    print("Opción 1: Borrar otro dato. Opción 2: Volver al menú")
                    opcion = int(input())
                    if opcion == 1:
                        pass
                    else:
                        break
            for j in lapellido:
                while borrar==j:
                    eliminar(lnombre)
                    eliminar(lapellido)
                    eliminar(larea)
                    eliminar(lingreso)
                    eliminar(lsalida)
                    eliminar(lobservacion)
                    print("Opción 1: Borrar otro dato. Opción 2: Volver al menú")
                    opcion = int(input())
                    if opcion == 1:
                        pass
                    else:
                        break
            pass
        else:
            break
