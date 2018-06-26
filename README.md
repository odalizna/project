# project
print("Bienvenido a la página de registros del Personal de Seguridad: Eulen Seguridad. de la Universidad de Ingeniería y Tecnología (UTEC)")
print("Si desea realizar cualquiera de las siguientes acciones, ingrese el número indicado:")
print("Una vez que haya realizado la acción, puede a volver a ingresar el mismo número si desea hacer la misma acción")
print("Acciones relacionadas con el ingreso del personal que labora en la universidad: 1")
print("Acciones relacionadas con el ingreso de visitantes: 2")
print("Acciones relacionadas con la pérdida de objetos: 3")
print("Acciones relacionadas con el ingreso de contratistas: 4")
print("Registro de alumnos sin carnet: 5")
print("Registro de las guías de remisión de los proveedores: 6")
print("Si deseas terminar o cancelar un proceso: 0")
print("Si deseas realizar otra acción: -1")
accion=10
lnombre=[]
lapellido=[]
larea=[]
ingresal={}
lobservacion=[]

while accion!=0:
    accion = int(input("Ingrese el número de la acción a realizar: "))
    print("Para realizar un nuevo registro: 7")
    print("Para realizar una búsqueda: 8")
    print("Para realizar una actualización de datos: 9")
    print("Para borrar un registro: 10")
    acción("Ingrese el nuevo número de acción:")
    if accion == 5:
        Motivo = ["Pérdida", "Robo", "Olvido"]
        RegistroCodigo = {}
        RegistroApellidoP = {}
        RegistroApellidoM = {}
        RegistroNombre = {}
        RegistroCiclo = {}
        RegistroEspecialidad = {}
        RegistroMotivo = {}
        
        pos = -1
        while pos != 0:
            Dni = str(input("Ingrese su número de DNI: "))
            if len(Dni) == 8:
                aviso = 1
                while aviso != 0:
                    Codigo = input("Ingrese su código de estudiante: ")
                    if len(Codigo) == 9:
                        RegistroCodigo[Dni]= Codigo
                        break
                    else:
                        print("Ingreso incorrecto de código de estudiante. Intente denuevo.")
                ApellidoP = str(input("Ingrese su apellido paterno: "))
                RegistroApellidoP[Dni] = ApellidoP
                ApellidoM = str(input("Ingrese su apellido materno: "))
                RegistroApellidoM[Dni] = ApellidoM
                Nombres = str(input("Ingrese sus nombres: "))
                RegistroNombre[Dni]=Nombres
                while aviso != 0:
                    Ciclo = int(input("Ingrese su número de ciclo: "))
                    if 0 <= Ciclo <= 10:
                        RegistroCiclo[Dni]= Ciclo
                        break
                    else:
                        print("Ingrese correctamente el ciclo que cursa")
                especialidad = str(input("Ingrese du especialidad: "))
                RegistroEspecialidad[Dni]= especialidad
                motivo = int(input("Tomando en cuenta que los motivos se encuentran en parámetros como los siguientes: Pérdida = 1, Robo = 2 y Olvido = 3. "
                                 "Ingrese el motivo por el que no posee Carnet: "))
                if motivo == 1:
                    MotivoR = Motivo[motivo-1]
                    RegistroMotivo[Dni] = MotivoR
                elif motivo ==2:
                    MotivoR = Motivo[motivo-1]
                    RegistroMotivo[Dni] = MotivoR
                elif motivo == 3:
                    MotivoR = Motivo[motivo-1]
                    RegistroMotivo[Dni] = MotivoR
                print("Si desea registrarse otro presiona 1, si desea culminar el proceso, presiona 2")
                Opcion = int(input())
                if Opcion == 1:
                    pass
                if Opcion ==2:
                    break
            else:
                print("Ingrese correctamente su número de DNI")
   elif accion==7:
        nombre=str(input("Ingrese el primer nombre: "))
        lnombre.append(nombre)

        apellido=str(input("Ingrese el primer apellido: "))
        lapellido.append(apellido)

        area=str(input("Ingrese el área al que pertenece: "))
        larea.append(area)

        ingreso=str(input("Ingrese la hora de ingreso (hh:mm): "))
        salida=str(input("Ingrese la hora de salida (hh:mm): "))
        ingresal.update({ingreso:salida})

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
                    for x in ingresal.keys():
                        print('El nombre completo de la persona es: {} {}, pertenece al area de {}, ingresó a las {} horas y salió a las {} horas'.format(busqueda,lapellidos[a],larea[a],,ingresol[a]))
                

    elif acción==9:
    elif acción==10:


    else:
        break
