lnombre=[]
lapellido=[]
lapellido2=[]
larea=[]
lingreso=[]
lsalida=[]
lobservacion=[]

lnombrevisit=[]
lapellidovisit=[]
lapellido2visit=[]
ldnivisit=[]
lautoriza=[]
lcorreovisit=[]
lingresovisit=[]
lsalidavisit=[]
lobservacionvisit=[]

lobjeto=[]
lmarca=[]
lcolor=[]
ltamano=[]
lhora=[]
llugar=[]

DNI = []
ApPaterno = []
ApMaterno = []
Nombre = []
Celular = []
Compania = []
Ciudad = []

NGuia = []
RUC = []
FEmision = []
Descripcion = []
Firma = []

def salida (o,n):
    if o in n:
        a=n.index(o)
        return('El nombre completo de la persona es: {}'.format(lnombre[a]), '{}'.format (lapellido[a]), {}.format (lapellido2[a]), 'que pertenece al area de {}'.format(larea[a]), 'ingresó a las {} horas'.format(lingreso[a]), 'y salió a las {} horas'.format(lsalida[a]))
    else:
        return('{} no existe'.format(o))
def salida2 (o,n):
    a=0
    if o in n:
        a=n.index(o)
        return('El nombre completo de la persona es: {} {} {}, con DNI {}, ingresó a las {} horas y salió a las {} horas, con la autorización de: {}'.format(lnombrevisit[a],lapellidovisit[a].lapellido2visit[a],ldnivisit[a],lingresovisit[a],lsalidavisit[a]),lautoriza[a])
    else:
        return('{} no existe'.format(o))

def actualizacion(lista,dato):
    posicion=0
    posicion=lista.index(actualizar)
    lista[posicion]=(dato)

def actualizardato1 ():
    print("Si desea actualizar otro dato de este mismo registro: 1")
    print("Si desea actualizar otro registro: 2")
    print("Si desea terminar su acción y volver al menú: 3")
    opcion=int(input("Ingrese su opción: "))
    if opcion==1:
        actualizar=1
    elif opcion==2:
        accion2=3
    else:
        accion2=0
        accion=-1

def actualizardato2 ():
    print("Si desea actualizar otro dato de este mismo registro: 1")
    print("Si desea actualizar otro registro: 2")
    print("Si desea terminar su acción y volver al menú: 3")
    opcion=int(input("Ingrese su opción: "))
    if opcion==1:
        actualizar=2
    elif opcion==2:
        accion2=3
    else:
        accion2=0
        accion=-1

def actualizardato3 ():
    print("Si desea actualizar otro dato de este mismo registro: 1")
    print("Si desea actualizar otro registro: 2")
    print("Si desea terminar su acción y volver al menú: 3")
    opcion=int(input("Ingrese su opción: "))
    if opcion==1:
        actualizarvisit=1
    elif opcion==2:
        accion2visit=3
    else:
        accion2visit=0
        accion=-1

def actualizardato4 ():
    print("Si desea actualizar otro dato de este mismo registro: 1")
    print("Si desea actualizar otro registro: 2")
    print("Si desea terminar su acción y volver al menú: 3")
    opcion=int(input("Ingrese su opción: "))
    if opcion==1:
        actualizarvisit=2
    elif opcion==2:
        accion2visit=3
    else:
        accion2visit=0
        accion=-1

def eliminar(lista,bo):
    posicion=0
    posicion=lista.index(bo)
    lista.pop(posicion)

def lee_entero1(mensaje):
    while True:
        valor = input(mensaje)
        try:
            valor = int(valor)
            return valor
        except ValueError:
            print("Error, sólo se permite dígitos numéricos, intente de nuevo...")
            pass

def lee_entero_entre1(mensaje, min, max):
    while True:
        valor = lee_entero1(mensaje)
        if min <= valor <= max:
            return valor
        else:
            print("Ingreso de número fuera del rango permitido, intente de nuevo...")

def lee_cadena_len_numeros1(mensaje, long):
    while True:
        valor = input(mensaje)
        if len(valor) == long:
            try:
                valor1 = int(valor)
                return valor
            except ValueError:
                print("Error, sólo se permite dígitos numéricos, intente de nuevo...")
                pass
        else:
                print("Error en cantidad de dígitos requeridos, intente de nuevo...")

def Menu_Principal1():
    print("")
    print("SISTEMA DE REGISTRO DE ALUMNOS SIN CARNET UNIVERSITARIO UTEC")
    print("")
    print("             [1] Agregar registro")
    print("             [2] Eliminar registro")
    print("             [3] Editar registro")
    print("             [4] Buscar registro")
    print("             [5] Listar registros")
    print("             [6] Abandonar sistema")
    print("")
    return lee_entero_entre1("Seleccione una opción de la tarea a realizar: ", 1, 6)

def Agregar1():
    print("")
    DNI1 = lee_cadena_len_numeros1("DNI                                     : ", 8)
    CodEstudiante1 = lee_cadena_len_numeros1("Código de estudiante                    : ", 9)
    ApPaterno1 = input("Apellido paterno                        : ").upper()
    ApMaterno1 = input("Apellido materno                        : ").upper()
    Nombre1 = input("Nombre                                  : ").upper()
    Ciclo1 = lee_entero_entre1("Ciclo                                   : ", 0, 10)
    Especialidad1 = input("Especialidad                            : ").upper()
    print("Los motivos por la que no cuentas con carnet pueden ser: ", MotivosNoCarnet)
    MotivoNoCarnet1 = lee_entero_entre1("Motivo por la que no cuentas con carnet : ", 1, 3)
    print("")
    opcion1 = lee_entero_entre1("Desea guardar los datos [1] = Si y [2] = No: ", 1, 2)
    if opcion1 == 1:
        DNI.append(DNI1)
        CodEstudiante.append(CodEstudiante1)
        ApPaterno.append(ApPaterno1)
        ApMaterno.append(ApMaterno1)
        Nombre.append(Nombre1)
        Ciclo.append(Ciclo1)
        Especialidad.append(Especialidad1)
        MotivoNoCarnet.append(MotivoNoCarnet1)

def Modificar1(Pos):
    print("")
    DNI1 = lee_cadena_len_numeros1("DNI                                     : " + DNI[Pos] + ": ", 8)
    CodEstudiante1 = lee_cadena_len_numeros1("Código de estudiante                    : " + CodEstudiante[Pos] + ": ", 9)
    ApPaterno1 = input("Apellido paterno                        : " + ApPaterno[Pos] + ": ").upper()
    ApMaterno1 = input("Apellido materno                        : " + ApMaterno[Pos] + ": ").upper()
    Nombre1 = input("Nombre                                  : " + Nombre[Pos] + ": ").upper()
    Ciclo1 = lee_entero_entre1("Ciclo                                   : " + str(Ciclo[Pos]) + ": ", 0, 10)
    Especialidad1 = input("Especialidad                            : " + Especialidad[Pos] + ": ").upper()
    print("Los motivos por la que no cuentas con carnet pueden ser: ", MotivosNoCarnet)
    MotivoNoCarnet1 = lee_entero_entre1("Motivo por la que no cuentas con carnet : " + str(MotivoNoCarnet[Pos]) + ": ", 1, 3)
    print("")
    opcion1 = lee_entero_entre1("Desea guardar los datos MODIFICADOS [1] = Si y [2] = No: ", 1, 2)
    if opcion1 == 1:
        DNI[Pos] = DNI1
        CodEstudiante[Pos] = CodEstudiante1
        ApPaterno[Pos] = ApPaterno1
        ApMaterno[Pos] = ApMaterno1
        Nombre[Pos] = Nombre1
        Ciclo[Pos] = Ciclo1
        Especialidad[Pos] = Especialidad1
        MotivoNoCarnet[Pos] = MotivoNoCarnet1

def Buscar1(Tarea, Mensaje):
    while True:
        opcion2 = Busqueda1(Mensaje)
        if opcion2 == 1:
            DNI1 = lee_cadena_len_numeros1("DNI                                     : ", 8)
            if DNI1 in DNI:
                Pos = DNI.index(DNI1)
            else:
                Pos = -1
        elif opcion2 == 2:
            CodEstudiante1 = lee_cadena_len_numeros1("Código de estudiante                    : ", 9)
            if CodEstudiante1 in CodEstudiante:
                Pos = CodEstudiante.index(CodEstudiante1)
            else:
                Pos = -1
        elif opcion2 == 3:
            ApPaterno1 = input("Apellido paterno                        : ").upper()
            if ApPaterno1 in ApPaterno:
                Pos = ApPaterno.index(ApPaterno1)
            else:
                Pos = -1
        elif opcion2 == 4:
            ApMaterno1 = input("Apellido materno                        : ").upper()
            if ApMaterno1 in ApMaterno:
                Pos = ApMaterno.index(ApMaterno1)
            else:
                Pos = -1
        elif opcion2 == 5:
            Nombre1 = input("Nombre                                  : ").upper()
            if Nombre1 in Nombre:
                Pos = Nombre.index(Nombre1)
            else:
                Pos = -1
        elif opcion2 == 6:
            break

        if Pos > -1:
            Mostrar1("BÚSQUEDA EXITOSA, DATOS DEL ALUMNO: ", Pos)
            if Tarea == 1:
                Eliminar1(Pos)
                print("Alumno ELIMINADO exitosamente...")
            elif Tarea == 2:
                Modificar1(Pos)
                print("Datos del Alumno MODIFICADO exitosamente...")
        else:
            print("Dato buscado no existe...")

def Busqueda1(Mensaje):
    print("")
    print(Mensaje)
    print("")
    print("[1] Buscar por DNI")
    print("[2] Buscar por código de estudiante")
    print("[3] Buscar por apellido paterno")
    print("[4] buscar por apellido materno")
    print("[5] Buscar por nombre")
    print("[6] Abandonar " + Mensaje)
    print("")
    return lee_entero_entre1("Seleccione una opción de la tarea a realizar: ", 1, 6)

def Mostrar1(Mensaje, Pos):
    print("")
    print(Mensaje)
    print("")
    print("DNI                       : ", AlumnosSinCarnet["DNI"][Pos])
    print("Código estudiante         : ", AlumnosSinCarnet["CodEstudiante"][Pos])
    print("Apellido Paterno          : ", AlumnosSinCarnet["ApPaterno"][Pos])
    print("Apellido Materno          : ", AlumnosSinCarnet["ApMaterno"][Pos])
    print("Nombre(s)                 : ", AlumnosSinCarnet["Nombre"][Pos])
    print("Ciclo                     : ", AlumnosSinCarnet["Ciclo"][Pos])
    print("Especialidad              : ", AlumnosSinCarnet["Especialidad"][Pos])
    print("Motivo por no tener Carnet ", MotivosNoCarnet, ": ", AlumnosSinCarnet["MotivoNoCarnet"][Pos])
    print("")

def Eliminar1(Pos):
    DNI.pop(Pos)
    CodEstudiante.pop(Pos)
    ApPaterno.pop(Pos)
    ApMaterno.pop(Pos)
    Nombre.pop(Pos)
    Ciclo.pop(Pos)
    Especialidad.pop(Pos)
    MotivoNoCarnet.pop(Pos)

def Listar():
    print("")
    print("        LISTADO DE ALUMNOS UNIVERSITARIOS UTEC QUE NO CUENTAN CON CARNET UNIVERSITARIO             ")
    print("---------------------------------------------------------------------------------------------------")
    print("DNI    Cód. Estud.    Ap. Paterno       Ap. Materno        Nombre(s)  Ciclo   Especialidad   Motivo")
    print("---------------------------------------------------------------------------------------------------")
    for i in range(len(DNI)):
        print(AlumnosSinCarnet["DNI"][i], end="   ")
        print(AlumnosSinCarnet["CodEstudiante"][i], end="   ")
        print(AlumnosSinCarnet["ApPaterno"][i], end="   ")
        print(AlumnosSinCarnet["ApMaterno"][i], end="   ")
        print(AlumnosSinCarnet["Nombre"][i], end="   ")
        print(AlumnosSinCarnet["Ciclo"][i], end="   ")
        print(AlumnosSinCarnet["Especialidad"][i], end="   ")
        print(AlumnosSinCarnet["MotivoNoCarnet"][i])
    print("---------------------------------------------------------------------------------------------------")
    print("")
def lee_entero2(mensaje):
    while True:
        valor = input(mensaje)
        try:
            valor = int(valor)
            return valor
        except ValueError:
            print("Error, sólo se permite dígitos numéricos, intente de nuevo...")
            pass

def lee_entero_entre2(mensaje, min, max):
    while True:
        valor = lee_entero2(mensaje)
        if min <= valor <= max:
            return valor
        else:
            print("Ingreso de número fuera del rango permitido, intente de nuevo...")

def lee_cadena_len_numeros2(mensaje, long):
    while True:
        valor = input(mensaje)
        if len(valor) == long:
            try:
                valor1 = int(valor)
                return valor
            except ValueError:
                print("Error, sólo se permite dígitos numéricos, intente de nuevo...")
                pass
        else:
                print("Error en cantidad de dígitos requeridos, intente de nuevo...")

def Menu_Principal2():
    print("")
    print("SISTEMA DE REGISTRO DE CONTRATISTAS")
    print("")
    print("             [1] Agregar registro")
    print("             [2] Eliminar registro")
    print("             [3] Editar registro")
    print("             [4] Buscar registro")
    print("             [5] Listar registros")
    print("             [6] Abandonar sistema")
    print("")
    return lee_entero_entre2("Seleccione una opción de la tarea a realizar: ", 1, 6)

def Agregar2():
    print("")
    DNI1 = lee_cadena_len_numeros2("DNI             : ", 8)
    ApPaterno1 = input("Apellido paterno: ").upper()
    ApMaterno1 = input("Apellido materno: ").upper()
    Nombre1 = input("Nombre          : ").upper()
    Celular1 = lee_cadena_len_numeros2("Celular         : ", 9)
    Compania1 = input("Compañia        : ").upper()
    Ciudad1 = input("Ciudad          : ").upper()
    print("")
    opcion1 = lee_entero_entre2("Desea guardar los datos [1] = Si y [2] = No: ", 1, 2)
    if opcion1 == 1:
        DNI.append(DNI1)
        ApPaterno.append(ApPaterno1)
        ApMaterno.append(ApMaterno1)
        Nombre.append(Nombre1)
        Celular.append(Celular1)
        Compania.append(Compania1)
        Ciudad.append(Ciudad1)

def Modificar2(Pos):
    print("")
    DNI1 = lee_cadena_len_numeros2("DNI             : " + DNI[Pos] + ": ", 8)
    ApPaterno1 = input("Apellido paterno: " + ApPaterno[Pos] + ": ").upper()
    ApMaterno1 = input("Apellido materno: " + ApMaterno[Pos] + ": ").upper()
    Nombre1 = input("Nombre          : " + Nombre[Pos] + ": ").upper()
    Celular1 = lee_cadena_len_numeros2("Celular         : " + Celular[Pos] + ": ", 9)
    Compania1 = input("Compañia        : " + Compania[Pos] + ": ").upper()
    Ciudad1 = input("Ciudad          : " + Ciudad[Pos] + ": ").upper()
    print("")
    opcion1 = lee_entero_entre2("Desea guardar los datos MODIFICADOS [1] = Si y [2] = No: ", 1, 2)
    if opcion1 == 1:
        DNI[Pos] = DNI1
        ApPaterno[Pos] = ApPaterno1
        ApMaterno[Pos] = ApMaterno1
        Nombre[Pos] = Nombre1
        Celular[Pos] = Celular1
        Compania[Pos] = Compania1
        Ciudad[Pos] = Ciudad1

def Buscar2(Tarea, Mensaje):
    while True:
        opcion2 = Busqueda2(Mensaje)
        if opcion2 == 1:
            DNI1 = lee_cadena_len_numeros2("DNI                                     : ", 8)
            if DNI1 in DNI:
                Pos = DNI.index(DNI1)
            else:
                Pos = -1
        elif opcion2 == 2:
            ApPaterno1 = input("Apellido paterno                        : ").upper()
            if ApPaterno1 in ApPaterno:
                Pos = ApPaterno.index(ApPaterno1)
            else:
                Pos = -1
        elif opcion2 == 3:
            ApMaterno1 = input("Apellido materno                        : ").upper()
            if ApMaterno1 in ApMaterno:
                Pos = ApMaterno.index(ApMaterno1)
            else:
                Pos = -1
        elif opcion2 == 4:
            Nombre1 = input("Nombre                                  : ").upper()
            if Nombre1 in Nombre:
                Pos = Nombre.index(Nombre1)
            else:
                Pos = -1
        elif opcion2 == 5:
            break

        if Pos > -1:
            Mostrar2("BÚSQUEDA EXITOSA, DATOS DEL CONTRATISTA: ", Pos)
            if Tarea == 1:
                Eliminar2(Pos)
                print("CONTRATISTA ELIMINADO exitosamente...")
            elif Tarea == 2:
                Modificar2(Pos)
                print("Datos del CONTRATISTA MODIFICADO exitosamente...")
        else:
            print("Dato buscado no existe...")

def Busqueda2(Mensaje):
    print("")
    print(Mensaje)
    print("")
    print("[1] Buscar por DNI")
    print("[2] Buscar por apellido paterno")
    print("[3] buscar por apellido materno")
    print("[4] Buscar por nombre")
    print("[5] Abandonar " + Mensaje)
    print("")
    return lee_entero_entre2("Seleccione una opción de la tarea a realizar: ", 1, 5)

def Mostrar2(Mensaje, Pos):
    print("")
    print(Mensaje)
    print("")
    print("DNI             : ", Contratistas["DNI"][Pos])
    print("Apellido Paterno: ", Contratistas["ApPaterno"][Pos])
    print("Apellido Materno: ", Contratistas["ApMaterno"][Pos])
    print("Nombre(s)       : ", Contratistas["Nombre"][Pos])
    print("Celular         : ", Contratistas["Celular"][Pos])
    print("Compañia        : ", Contratistas["Compañia"][Pos])
    print("Ciudad          : ", Contratistas["Ciudad"][Pos])
    print("")

def Eliminar2(Pos):
    DNI.pop(Pos)
    ApPaterno.pop(Pos)
    ApMaterno.pop(Pos)
    Nombre.pop(Pos)
    Celular.pop(Pos)
    Compania.pop(Pos)
    Ciudad.pop(Pos)

def Listar2():
    print("")
    print("        LISTADO DE CONTRATISTAS             ")
    print("-----------------------------------------------------------------------------------")
    print("DNI    Ap. Paterno     Ap. Materno     Nombre(s)  Celular      Compañia      Ciudad")
    print("-----------------------------------------------------------------------------------")
    for i in range(len(DNI)):
        print(Contratistas["DNI"][i], end="   ")
        print(Contratistas["ApPaterno"][i], end="   ")
        print(Contratistas["ApMaterno"][i], end="   ")
        print(Contratistas["Nombre"][i], end="   ")
        print(Contratistas["Celular"][i], end="   ")
        print(Contratistas["Compañia"][i], end="   ")
        print(Contratistas["Ciudad"][i])
    print("-----------------------------------------------------------------------------------")
    print("")

DNI = []
CodEstudiante = []
ApPaterno = []
ApMaterno = []
Nombre = []
Ciclo = []
Especialidad = []
MotivoNoCarnet = []
MotivosNoCarnet = ["{1} = Pérdida", "{2} = Robo", "{3} = Olvido"]
AlumnosSinCarnet = {"DNI" : DNI, "CodEstudiante" : CodEstudiante, "ApPaterno" : ApPaterno, "ApMaterno" : ApMaterno, "Nombre" : Nombre, "Ciclo" : Ciclo, "Especialidad" : Especialidad, "MotivoNoCarnet" : MotivoNoCarnet}


def lee_entero(mensaje):
    while True:
        valor = input(mensaje)
        try:
            valor = int(valor)
            return valor
        except ValueError:
            print("Error, sólo se permite dígitos numéricos, intente de nuevo...")
            pass

def lee_entero_entre(mensaje, min, max):
    while True:
        valor = lee_entero(mensaje)
        if min <= valor <= max:
            return valor
        else:
            print("Ingreso de número fuera del rango permitido, intente de nuevo...")

def lee_cadena_len_numeros(mensaje, long):
    while True:
        valor = input(mensaje)
        if len(valor) == long:
            try:
                valor1 = int(valor)
                return valor
            except ValueError:
                print("Error, sólo se permite dígitos numéricos, intente de nuevo...")
                pass
        else:
                print("Error en cantidad de dígitos requeridos, intente de nuevo...")

def Menu_Principal():
    print("")
    print("SISTEMA DE CONTROL DE GUÍAS DE REMISIÓN")
    print("")
    print("       [1] Agregar registro")
    print("       [2] Eliminar registro")
    print("       [3] Editar registro")
    print("       [4] Buscar registro")
    print("       [5] Listar registros")
    print("       [6] Abandonar sistema")
    print("")
    return lee_entero_entre("Seleccione una opción de la tarea a realizar: ", 1, 6)

def Agregar():
    print("")
    NGuia1 = lee_cadena_len_numeros("Nº de guía   : ", 6)
    RUC1 = lee_cadena_len_numeros("R.U.C.       : ", 11)
    FEmision1 = input("Fecha emisión: ")
    Descripcion1 = input("Descripción  : ").upper()
    Firma1 = input("Firma        : ").upper()
    print("")
    opcion1 = lee_entero_entre("Desea guardar los datos [1] = Si y [2] = No: ", 1, 2)
    if opcion1 == 1:
        NGuia.append(NGuia1)
        RUC.append(RUC1)
        FEmision.append(FEmision1)
        Descripcion.append(Descripcion1)
        Firma.append(Firma1)

def Modificar(Pos):
    print("")
    NGuia1 = lee_cadena_len_numeros("Nº de guía   : " + NGuia[Pos] + ": ", 6)
    RUC1 = lee_cadena_len_numeros("R.U.C.       : " + RUC[Pos] + ": ", 11)
    FEmision1 = input("Fecha emisión: " + FEmision[Pos] + ": ")
    Descripcion1 = input("Descripción  : " + Descripcion[Pos] + ": ").upper()
    Firma1 = input("Firma        : " + Firma[Pos] + ": ").upper()
    print("")
    opcion1 = lee_entero_entre("Desea guardar los datos MODIFICADOS [1] = Si y [2] = No: ", 1, 2)
    if opcion1 == 1:
        NGuia[Pos] = NGuia1
        RUC[Pos] = RUC1
        FEmision[Pos] = FEmision1
        Descripcion[Pos] = Descripcion1
        Firma[Pos] = Firma1

def Buscar(Tarea, Mensaje):
    while True:
        opcion2 = Busqueda(Mensaje)
        if opcion2 == 1:
            NGuia1 = lee_cadena_len_numeros("Nº de guía   : ", 6)
            if NGuia1 in NGuia:
                Pos = NGuia.index(NGuia1)
            else:
                Pos = -1
        elif opcion2 == 2:
            RUC1 = lee_cadena_len_numeros("R.U.C.       : ", 11)
            if RUC1 in RUC:
                Pos = RUC.index(RUC1)
            else:
                Pos = -1
        elif opcion2 == 3:
            break

        if Pos > -1:
            Mostrar("BÚSQUEDA EXITOSA, DATOS DE LA GUÍA: ", Pos)
            if Tarea == 1:
                Eliminar(Pos)
                print("GUÍA ELIMINADA exitosamente...")
            elif Tarea == 2:
                Modificar(Pos)
                print("Datos de GUÍA MODIFICADA exitosamente...")
        else:
            print("Dato buscado no existe...")

def Busqueda(Mensaje):
    print("")
    print(Mensaje)
    print("")
    print("[1] Buscar por Nº de Guía")
    print("[2] Buscar por R.U.C.")
    print("[3] Abandonar " + Mensaje)
    print("")
    return lee_entero_entre("Seleccione una opción de la tarea a realizar: ", 1, 3)

def Mostrar(Mensaje, Pos):
    print("")
    print(Mensaje)
    print("")
    print("Nº Guía      : ", Guias["NGuia"][Pos])
    print("R.U.C.       : ", Guias["RUC"][Pos])
    print("Fecha Emisión: ", Guias["FEmision"][Pos])
    print("Descripción  : ", Guias["Descripcion"][Pos])
    print("Firma        : ", Guias["Firma"][Pos])
    print("")

def Eliminar(Pos):
    NGuia.pop(Pos)
    RUC.pop(Pos)
    FEmision.pop(Pos)
    Descripcion.pop(Pos)
    Firma.pop(Pos)

def Listar():
    print("")
    print("        LISTADO DE GUÍAS             ")
    print("-----------------------------------------------------------------------------------")
    print("Nº Guía     R.U.C.       Fecha Emisión  Descripción                     Firma      ")
    print("-----------------------------------------------------------------------------------")
    for i in range(len(NGuia)):
        print(Guias["NGuia"][i], end="   ")
        print(Guias["RUC"][i], end="   ")
        print(Guias["FEmision"][i], end="   ")
        print(Guias["Descripcion"][i], end="   ")
        print(Guias["Firma"][i])
    print("-----------------------------------------------------------------------------------")
    print("")

accion=-1
while accion==-1:
    print("************************************************************************")
    print("     Bienvenido a la página de registros del Personal de Seguridad:")
    print("     'Eulen' de la Universidad de Ingeniería y Tecnología (UTEC)")
    print("************************************************************************")
    print("Si desea realizar cualquiera de las siguientes acciones, ingrese el número indicado:")
    print("")
    print("Acciones relacionadas con:                           | Número a ingresar: ")
    print("-----------------------------------------------------|-------------------")
    print("Ingreso del personal que labora en la universidad    |        1")
    print("Ingreso de visitantes                                |        2")
    print("Pérdida de objetos                                   |        3")
    print("Registro de alumnos sin carnet                       |        4")
    print("Ingreso de contratistas                              |        5")
    print("Registro de las guías de remisión de los proveedores |        6")
    print("***************************************************************************")
    accion=int(input("El número de acción elegido es: "))
    while accion==1:
        print("************************************************")
        print("Ingrese el número de acción que desea realizar:")
        print("Nuevo registro:           1")
        print("Búsqueda:                 2")
        print("Actualización de datos:   3")
        print("Borrar un registro:       4")
        accion2=int(input("Ingrese su nuevo número: "))
        while accion2==1:
            nombre=input("Ingrese el primer nombre: ")
            lnombre.append(nombre)

            apellido=str(input("Ingrese el primer apellido: "))
            lapellido.append(apellido)

            apellido2=str(input("Ingrese el segundo apellido: "))
            lapellido2.append(apellido2)

            area=str(input("Ingrese el área al que pertenece: "))
            larea.append(area)

            ingreso=str(input("Ingrese la hora de ingreso (hh:mm): "))
            lingreso.append(ingreso)

            horasalida=str(input("Ingrese la hora de salida (hh:mm): "))
            lsalida.append(horasalida)

            observacion=str(input("Ingrese cualquier observación adicional o SO (Sin Observación): "))
            lobservacion.append(observacion)
            print("Se ha realizado su registro correctamente")
            print("Si desea hacer otro registro: 1")
            print("Si desea terminar su acción y volver al menú: 2")
            opcion=int(input("Ingrese su opción: "))
            if opcion==1:
                accion2=1
            else:
                accion2=0
                accion=-1
        while accion2==2:
            print("*********************************")
            print("Búsqueda por nombre:          1")
            print("Búsqueda por apellido:        2")
            print("Búsqueda por área:            3")
            print("Búsqueda por hora de ingreso: 4")
            eleccion3=int(input("Ingrese el tipo de búsqueda: "))
            if eleccion3==1:
                #busqueda = str(input("Ingrese el nombre que desea buscar: "))
                busqueda=str(input("Ingrese el nombre que desea buscar: "))
                print(salida(busqueda,lnombre))
            elif eleccion3==2:
                busqueda1 = str(input("Ingrese el apellido (primer apellido) que desea buscar: "))
                print(salida(busqueda1,lapellido))
            elif eleccion3==3:
                busqueda2 = str(input("Ingrese el area de la que desea que aparezca la cantidad y las personas que ingresaron: "))
                a=0
                cont=0
                for x in larea:
                    if x == busqueda2:
                        cont = cont +1
                        a=larea.index(busqueda2)
                        print('La cantidad de personas del área de {}, que ingresaron fueron {}'.format(busqueda,cont))
                        print('El nombre completo de la persona es: {} {} {}, que pertenece al area de {}, ingresó a las {} horas y salió a las {} horas'.format(lnombre[a],lapellido[a].lapellido2[a],larea[a],lingreso[a],lsalida[a]))
                    else:
                        print('{} no existe'.format(busqueda2))
            elif eleccion3==4:
                busqueda3 = str(input("Ingrese la hora de ingreso para buscar a la persona por este criterio: "))
                print(salida(busqueda3,lingreso))
            else:
                print("Ingrese un valor aceptable")
                accion2=2
            print("Si desea buscar otro dato: 1")
            print("Si desea terminar su acción y volver al menú: 2")
            opcion=int(input("Ingrese su opción: "))
            if opcion==1:
                accion2=1
            else:
                accion2=0
                accion=-1
        while accion2==3:
            actualizar = str(input("Ingrese el nombre o el primer apellido del registro que quiere actualizar: "))

            while actualizar in lnombre or actualizar==1:
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
                    print("Si desea actualizar otro dato de este mismo registro: 1")
                    print("Si desea actualizar otro registro: 2")
                    print("Si desea terminar su acción y volver al menú: 3")
                    opcion=int(input("Ingrese su opción: "))
                    if opcion==1:
                        actualizar=1
                    elif opcion==2:
                        accion2=3
                    else:
                        accion2=0
                        accion=-1

                if datoac==2:
                    apellidoac=str(input("Ingrese el nuevo primer apellido: "))
                    actualizacion(lapellido,apellidoac)
                    print("Si desea actualizar otro dato de este mismo registro: 1")
                    print("Si desea actualizar otro registro: 2")
                    print("Si desea terminar su acción y volver al menú: 3")
                    opcion=int(input("Ingrese su opción: "))
                    if opcion==1:
                        actualizar=1
                    elif opcion==2:
                        accion2=3
                    else:
                        accion2=0
                        accion=-1
                if datoac==3:
                    apellido2ac=str(input("Ingrese el nuevo segundo apellido: "))
                    actualizacion(lapellido2,apellido2ac)
                    print("Si desea actualizar otro dato de este mismo registro: 1")
                    print("Si desea actualizar otro registro: 2")
                    print("Si desea terminar su acción y volver al menú: 3")
                    opcion=int(input("Ingrese su opción: "))
                    if opcion==1:
                        actualizar=1
                    elif opcion==2:
                        accion2=3
                    else:
                        accion2=0
                        accion=-1

                if datoac==4:
                    ingresoac=str(input("Ingrese la nueva hora de ingreso (hh:mm): "))
                    actualizacion(lingreso,ingresoac)
                    print("Si desea actualizar otro dato de este mismo registro: 1")
                    print("Si desea actualizar otro registro: 2")
                    print("Si desea terminar su acción y volver al menú: 3")
                    opcion=int(input("Ingrese su opción: "))
                    if opcion==1:
                        actualizar=1
                    elif opcion==2:
                        accion2=3
                    else:
                        accion2=0
                        accion=-1

                if datoac==5:
                    salidaac=str(input("Ingrese la nueva hora de salida (hh:mm): "))
                    actualizacion(lsalida,salidaac)
                    print("Si desea actualizar otro dato de este mismo registro: 1")
                    print("Si desea actualizar otro registro: 2")
                    print("Si desea terminar su acción y volver al menú: 3")
                    opcion=int(input("Ingrese su opción: "))
                    if opcion==1:
                        actualizar=1
                    elif opcion==2:
                        accion2=3
                    else:
                        accion2=0
                        accion=-1

            while actualizar in lapellido or actualizar==2:
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
                    print("Si desea actualizar otro dato de este mismo registro: 1")
                    print("Si desea actualizar otro registro: 2")
                    print("Si desea terminar su acción y volver al menú: 3")
                    opcion=int(input("Ingrese su opción: "))
                    if opcion==1:
                        actualizar=2
                    elif opcion==2:
                        accion2=3
                    else:
                        accion2=0
                        accion=-1

                if datoac==2:
                    apellidoac=str(input("Ingrese el nuevo primer apellido: "))
                    actualizacion(lapellido,apellidoac)
                    print("Si desea actualizar otro dato de este mismo registro: 1")
                    print("Si desea actualizar otro registro: 2")
                    print("Si desea terminar su acción y volver al menú: 3")
                    opcion=int(input("Ingrese su opción: "))
                    if opcion==1:
                        actualizar=2
                    elif opcion==2:
                        accion2=3
                    else:
                        accion2=0
                        accion=-1

                if datoac==3:
                    apellido2ac=str(input("Ingrese el nuevo segundo apellido: "))
                    actualizacion(lapellido2,apellido2ac)
                    print("Si desea actualizar otro dato de este mismo registro: 1")
                    print("Si desea actualizar otro registro: 2")
                    print("Si desea terminar su acción y volver al menú: 3")
                    opcion=int(input("Ingrese su opción: "))
                    if opcion==1:
                        actualizar=2
                    elif opcion==2:
                        accion2=3
                    else:
                        accion2=0
                        accion=-1
                if datoac==4:
                    ingresoac=str(input("Ingrese la nueva hora de ingreso (hh:mm): "))
                    actualizacion(lingreso,ingresoac)
                    print("Si desea actualizar otro dato de este mismo registro: 1")
                    print("Si desea actualizar otro registro: 2")
                    print("Si desea terminar su acción y volver al menú: 3")
                    opcion=int(input("Ingrese su opción: "))
                    if opcion==1:
                        actualizar=2
                    elif opcion==2:
                        accion2=3
                    else:
                        accion2=0
                        accion=-1

                if datoac==5:
                    salidaac=str(input("Ingrese la nueva hora de salida (hh:mm): "))
                    actualizacion(lsalida,salidaac)
                    print("Si desea actualizar otro dato de este mismo registro: 1")
                    print("Si desea actualizar otro registro: 2")
                    print("Si desea terminar su acción y volver al menú: 3")
                    opcion=int(input("Ingrese su opción: "))
                    if opcion==1:
                        actualizar=2
                    elif opcion==2:
                        accion2=3
                    else:
                        accion2=0
                        accion=-1

        while accion2==4:
            borrar = str(input("Ingrese el nombre o el primer apellido del registro que quiere borrar: "))
            for i in lnombre:
                while borrar==i:
                    eliminar(lnombre,borrar)
                    eliminar(lapellido,borrar)
                    eliminar(larea,borrar)
                    eliminar(lingreso,borrar)
                    eliminar(lsalida,borrar)
                    eliminar(lobservacion,borrar)
                    print("Si desea borrar otro registro: 1")
                    print("Si desea terminar su acción y volver al menú: 2")
                    opcion=int(input("Ingrese su opción: "))
                    if opcion==1:
                        accion2=4
                    else:
                        accion2=0
                        accion=-1

            for j in lapellido:
                while borrar==j:
                    eliminar(lnombre,borrar)
                    eliminar(lapellido,borrar)
                    eliminar(larea,borrar)
                    eliminar(lingreso,borrar)
                    eliminar(lsalida,borrar)
                    eliminar(lobservacion,borrar)
                    print("Si desea borrar otro registro: 1")
                    print("Si desea terminar su acción y volver al menú: 2")
                    opcion=int(input("Ingrese su opción: "))
                    if opcion==1:
                        accion2=4
                    else:
                        accion2=0
                        accion=-1
    while accion==2:
        print("************************************************")
        print("Ingrese el número de acción que desea realizar:")
        print("Nuevo registro:           1")
        print("Búsqueda:                 2")
        print("Actualización de datos:   3")
        print("Borrar un registro:       4")
        accion2visit=int(input("Ingrese su nuevo número: "))
        while accion2visit==1:
            nombrevisit=str(input("Ingrese el primer nombre: "))
            lnombrevisit.append(nombrevisit)

            apellidovisit=str(input("Ingrese el primer apellido: "))
            lapellidovisit.append(apellidovisit)

            apellido2visit=str(input("Ingrese el segundo apellido: "))
            lapellido2visit.append(apellido2visit)

            dnivisit=str(input("Ingrese el DNI del visitante: "))
            ldnivisit.append(dnivisit)

            autoriza=str(input("Ingrese la persona que autoriza: "))
            lautoriza.append(autoriza)

            correovisit=str(input("Ingrese el correo del visitante: "))
            lcorreovisit.append(correovisit)

            ingresovisit=str(input("Ingrese la hora de ingreso (hh:mm): "))
            lingresovisit.append(ingresovisit)

            salidavisit=str(input("Ingrese la hora de salida (hh:mm): "))
            lsalidavisit.append(salidavisit)

            observacionvisit=str(input("Ingrese cualquier observación adicional o SO (Sin Observación): "))
            lobservacionvisit.append(observacionvisit)

            print("Se ha realizado su registro correctamente")
            print("Si desea hacer otro registro: 1")
            print("Si desea terminar su acción y volver al menú: 2")
            opcion=int(input("Ingrese su opción: "))
            if opcion==1:
                accion2visit=2
            else:
                accion2visit=0
                accion=-1
        while accion2visit==2:
            print("*********************************")
            print("Búsqueda por nombre:          1")
            print("Búsqueda por apellido:        2")
            print("Búsqueda por DNI:            3")
            print("Búsqueda por hora de ingreso: 4")
            eleccion3=int(input("Ingrese el tipo de búsqueda: "))
            if eleccion3==1:
                busqueda = str(input("Ingrese el nombre que desea buscar: "))
                print(salida2(busqueda,lnombrevisit))
            elif eleccion3==2:
                busqueda1 = str(input("Ingrese el apellido (primer apellido) que desea buscar: "))
                print(salida2(busqueda1,lapellidovisit))
            elif eleccion3==3:
                busqueda2 = str(input("Ingrese el DNI que desea buscar "))
                print(salida2(busqueda2,ldnivisit))
            elif eleccion3==4:
                busqueda3 = str(input("Ingrese la hora de ingreso para buscar a la persona por este criterio: "))
                print(salida2(busqueda3,lingresovisit))
            else:
                print("Ingrese un valor aceptable")
                accion2=2
            print("Si desea buscar otro dato: 1")
            print("Si desea terminar su acción y volver al menú: 2")
            opcion=int(input("Ingrese su opción: "))
            if opcion==1:
                accion2visit=2
            else:
                accion2visit=0
                accion=-1
        while accion2visit==3:
            actualizarvisit = str(input("Ingrese el nombre o el primer apellido del registro que quiere actualizar: "))
            while actualizarvisit in lnombrevisit or actualizarvisit==1:
                print("¿Qué dato desea actualizar?")
                print("Nombre: 1")
                print("Primer apellido: 2")
                print("Segundo apellido: 3")
                print("DNI: 4")
                print("Persona que autoriza: 5")
                print("Correo: 6")
                print("La hora de ingreso: 7")
                print("La hora de salida: 8")
                datoac=int(input("Ingrese el número del tipo de dato a actualizar: "))

                if datoac==1:
                    nombreacvisit=str(input("Ingrese el nuevo nombre: "))
                    actualizacion(lnombrevisit,nombreacvisit)
                    actualizardato3()

                if datoac==2:
                    apellidoacvisit=str(input("Ingrese el nuevo primer apellido: "))
                    actualizacion(lapellidovisit,apellidoacvisit)
                    actualizardato3()
                if datoac==3:
                    apellido2acvisit=str(input("Ingrese el nuevo segundo apellido: "))
                    actualizacion(lapellido2visit,apellido2acvisit)
                    actualizardato3()
                if datoac==4:
                    dniacvisit=str(input("Ingrese el nuevo DNI: "))
                    actualizacion(ldnivisit,dniacvisit)
                    actualizardato3()
                if datoac==5:
                    autorizaactvisit=str(input("Ingrese la nueva persona que autoriza: "))
                    actualizacion(lautoriza,autorizaactvisit)
                    actualizardato3()
                if datoac==6:
                    ingresoacvisit=str(input("Ingrese la nueva hora de ingreso (hh:mm): "))
                    actualizacion(lingresovisit,ingresoacvisit)
                    actualizardato3()
                if datoac==7:
                    salidaacvisit=str(input("Ingrese la nueva hora de salida (hh:mm): "))
                    actualizacion(lsalidavisit,salidaacvisit)
                    actualizardato3()
            while actualizarvisit in lapellidovisit or actualizarvisit==2:
                print("¿Qué dato desea actualizar?")
                print("Nombre: 1")
                print("Primer apellido: 2")
                print("Segundo apellido: 3")
                print("DNI: 4")
                print("Persona que autoriza: 5")
                print("Correo: 6")
                print("La hora de ingreso: 7")
                print("La hora de salida: 8")
                datoac=int(input("Ingrese el número del tipo de dato a actualizar: "))

                if datoac==1:
                    nombreacvisit=str(input("Ingrese el nuevo nombre: "))
                    actualizacion(lnombrevisit,nombreacvisit)
                    actualizardato4()

                if datoac==2:
                    apellidoacvisit=str(input("Ingrese el nuevo primer apellido: "))
                    actualizacion(lapellidovisit,apellidoacvisit)
                    actualizardato4()
                if datoac==3:
                    apellido2acvisit=str(input("Ingrese el nuevo segundo apellido: "))
                    actualizacion(lapellido2visit,apellido2acvisit)
                    actualizardato4()
                if datoac==4:
                    dniacvisit=str(input("Ingrese el nuevo DNI: "))
                    actualizacion(ldnivisit,dniacvisit)
                    actualizardato4()
                if datoac==5:
                    autorizaactvisit=str(input("Ingrese la nueva persona que autoriza: "))
                    actualizacion(lautoriza,autorizaactvisit)
                    actualizardato4()
                if datoac==6:
                    ingresoacvisit=str(input("Ingrese la nueva hora de ingreso (hh:mm): "))
                    actualizacion(lingresovisit,ingresoacvisit)
                    actualizardato4()
                if datoac==7:
                    salidaacvisit=str(input("Ingrese la nueva hora de salida (hh:mm): "))
                    actualizacion(lsalidavisit,salidaacvisit)
                    actualizardato4()

        while accion2visit==4:
            borrarvisit = str(input("Ingrese el nombre o el primer apellido del registro que quiere borrar: "))
            for i in lnombrevisit:
                while borrarvisit==i:
                    eliminar(lnombrevisit,borrarvisit)
                    eliminar(lapellidovisit,borrarvisit)
                    eliminar(ldnivisit,borrarvisit)
                    eliminar(lautoriza,borrarvisit)
                    eliminar(lcorreovisit,borrarvisit)
                    eliminar(lingreso,borrarvisit)
                    eliminar(lsalida,borrarvisit)
                    eliminar(lobservacion,borrarvisit)
                    print("Si desea borrar otro registro: 1")
                    print("Si desea terminar su acción y volver al menú: 2")
                    opcion=int(input("Ingrese su opción: "))
                    if opcion==1:
                        accion2visit=4
                    else:
                        accion2visit=0
                        accion=-1

            for j in lapellidovisit:
                while borrarvisit==j:
                    eliminar(lnombrevisit,borrarvisit)
                    eliminar(lapellidovisit,borrarvisit)
                    eliminar(ldnivisit,borrarvisit)
                    eliminar(lautoriza,borrarvisit)
                    eliminar(lcorreovisit,borrarvisit)
                    eliminar(lingreso,borrarvisit)
                    eliminar(lsalida,borrarvisit)
                    eliminar(lobservacion,borrarvisit)
                    print("Si desea borrar otro registro: 1")
                    print("Si desea terminar su acción y volver al menú: 2")
                    opcion=int(input("Ingrese su opción: "))
                    if opcion==1:
                        accion2visit=4
                    else:
                        accion2visit=0
                        accion=-1
    while accion==3:
        print("************************************************")
        print("Ingrese el número de acción que desea realizar:")
        print("Nuevo registro:           1")
        print("Búsqueda:                 2")
        print("Borrar un registro:       4")
        accion2obj=int(input("Ingrese su nuevo número: "))
        while accion2obj==1:
            nombreobj=str(input("Ingrese el nombre del objeto encontrado: "))
            lobjeto.append(nombreobj)

            marcaobj=str(input("Ingrese la marca del objeto encontrado: "))
            lmarca.append(marcaobj)

            colorobj=str(input("Ingrese el color del objeto: "))
            lcolor.append(colorobj)

            tamano=str(input("Ingrese el tamaño del objeto (grande, mediano o pequeño): "))
            ltamano.append(tamano)

            horaobj=str(input("Ingrese la hora en la que fue encontrado: "))
            lhora.append(horaobj)

            lugarobj=str(input("Ingrese el lugar en el que fue encontrado: "))
            llugar.append(lugarobj)

            print("Se ha realizado su registro correctamente")
            print("Si desea hacer otro registro: 1")
            print("Si desea terminar su acción y volver al menú: 2")
            opcion=int(input("Ingrese su opción: "))
            if opcion==1:
                accion2obj=1
            else:
                accion2obj=0
                accion=-1
        while accion2obj==2:
            busqueda = str(input("Ingrese el nombre del objeto que desea buscar: "))
            print(salida2(busqueda,lnombreobj))
            a=0
            if busqueda in lnombreobj:
                a=lnombreobj.index(busqueda)
                print('El objeto perdido es: {}, de la marca {}, de color {}, de tamaño {}, que se encontró a las {} en {}'.format(lnombreobj[a],lmarca[a].lcolor[a],ltamano[a],lhora[a],llugar[a]))
            else:
                print('{} no existe'.format(busqueda))
            print("Si desea buscar otro objeto: 1")
            print("Si desea terminar su acción y volver al menú: 2")
            opcion=int(input("Ingrese su opción: "))
            if opcion==1:
                accion2obj=2
            else:
                accion2obj=0
                accion=-1

        while accion2obj==3:
            borrarobj = str(input("Ingrese el nombre del objeto que desea borrar: "))
            for i in lnombreobj:
                while borrarobj==i:
                    eliminar(lnombreobj,borrarobj)
                    eliminar(lmarca,borrarobj)
                    eliminar(lcolor,borrarobj)
                    eliminar(ltamano,borrarobj)
                    eliminar(lhora,borrarobj)
                    eliminar(llugar,borrarobj)
                    eliminar(lsalida,borrarobj)
                    print("Si desea borrar otro registro: 1")
                    print("Si desea terminar su acción y volver al menú: 2")
                    opcion=int(input("Ingrese su opción: "))
                    if opcion==1:
                        accion2obj=3
                    else:
                        accion2obj=0
                        accion=-1
    while accion==4:
        opcion = Menu_Principal1()
        if opcion == 1:
            Agregar1()
        elif opcion == 2:
            Buscar1(1, "ELIMINAR:")
        elif opcion == 3:
            Buscar1(2, "MODIFICAR:")
        elif opcion == 4:
            Buscar1(0, "BUSCAR:")
        elif opcion == 5:
            Listar()
        print("Si desea realizar otra acción acerca del registro de alumnos sin carnet : 1")
        print("Si desea terminar su acción y volver al menú: 2")
        opcion=int(input("Ingrese su opción: "))
        if opcion==1:
            accion=4
        else:
            accion=0
            accion=-1

#Contratistas

    while accion==5:

        Contratistas = {"DNI" : DNI, "ApPaterno" : ApPaterno, "ApMaterno" : ApMaterno, "Nombre" : Nombre, "Celular" : Celular, "Compañia" : Compania, "Ciudad" : Ciudad}
        opcion = Menu_Principal2()
        if opcion == 1:
            Agregar2()
        elif opcion == 2:
            Buscar2(1, "ELIMINAR:")
        elif opcion == 3:
            Buscar2(2, "MODIFICAR:")
        elif opcion == 4:
            Buscar2(0, "BUSCAR:")
        elif opcion == 5:
            Listar2()
        print("Si desea realizar otra acción acerca del registro de contratistas : 1")
        print("Si desea terminar su acción y volver al menú: 2")
        opcion=int(input("Ingrese su opción: "))
        if opcion==1:
            accion=5
        else:
            accion=0
            accion=-1
    while accion==6:
        Guias = {"NGuia" : NGuia, "RUC" : RUC, "FEmision" : FEmision, "Descripcion" : Descripcion, "Firma" : Firma}
        opcion = Menu_Principal()
        if opcion == 1:
            Agregar()
        elif opcion == 2:
            Buscar(1, "ELIMINAR:")
        elif opcion == 3:
            Buscar(2, "MODIFICAR:")
        elif opcion == 4:
            Buscar(0, "BUSCAR:")
        elif opcion == 5:
            Listar()
        print("Si desea realizar otra acción acerca del registro de remisión de guías : 1")
        print("Si desea terminar su acción y volver al menú: 2")
        opcion=int(input("Ingrese su opción: "))
        if opcion==1:
            accion=6
        else:
            accion=0
            accion=-1
