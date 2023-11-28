# Repositorio-practicas-
Prcticas en introduccion a la computacion 
def es_correo_electronico(cadena):
    # Verificar la presencia del carácter '@'
    if '@' not in cadena:
        return False
    
    # Dividir la cadena en dos partes: nombre de usuario y dominio
    usuario, dominio = cadena.split('@', 1)
    
    # Verificar las terminaciones del dominio
    if dominio.endswith('.com') or dominio.endswith('.com.mx') or dominio.endswith('.mx'):
        return True
    else:
        return False

# Pedir al usuario que ingrese una cadena de texto
cadena_ingresada = input("Ingrese una cadena de texto: ")

# Verificar si la cadena es un correo electrónico
if es_correo_electronico(cadena_ingresada):
    print("La cadena es un correo electrónico válido.")
else:
    print("La cadena no es un correo electrónico válido.")
