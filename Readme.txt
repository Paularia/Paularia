# un diccionario que almacena todos los datos
contactos = {"Paula" : "Paula","Paula" : "Sieira García", "Paula" : "555 55 55 55",
"Gloria": "Gloria", "Gloria": "Uzal Agra","Gloria": "999 99 99 99",
"Marta" : "Marta", "Marta" : "López De la Rosa", "Marta" : "777 55 77 99" }

  

#  las 5 opciones del menú
def menu():
 

print = ("1. Guardar contacto")
    
print = ("2. Ver contactos")
    
print = ("3. Eliminar contacto")
    
print = ("4. Editar contacto")
    
print = ("5. Salir")



selec = input("Elige la opción")



# si se elige la opción 1, se añadirá un contacto nuevo
if selec == "1":
    
    nombre = input("Nombre: ")   # se pregunta el nombre, appelidos y número
    
    apellidos = input("Apellidos: ")
    
    numero = input("Número: ")
    
    contactos["Nombre"] = nombre
  # se añade al diccionario  
    contactos["Apellidos"] = apellidos
    
    contactos["Número"] = numero
    
    print (contactos)

   

# si la opción es 2, se se escriben todos los contactos 
elif selec == "2":
    
    print(contactos)


# en la opción 3 se elimina un contacto
elif selec == "3":
    
    elim = input("Elige el contacto a eliminar")
    # se pregunta el contacto a eliminar
   if elim in contactos:
       
      del contactos[elim]
    # se elimina y se escribe la nueva lista    
      print (contactos)
    
  else:
        
      print ("Ese contacto no existe")

    # en caso de no existir      


# si la opción es 4 se puede editar un contacto
elif selec == "4":
    
     ed = input("Elige el contacto que quieras editar")
   # se elige el contacto a editar    
  if ed in contactos:
        
     nom = input("Nombre: ")   # se pregunta el nombre, apellidos y número nuevos
        
     apell = input("Apellidos: ")
        
     numer = input("Número: ")
        
     contactos[ed] = nom
        # se sustituye en el diccionario
     contactos[ed] = apell
        
     contactos[ed] = numer
        
     print (contactos)

    
  else:
        
     print ("Ese contacto no existe")
   # en caso de no existir        



elif selec == "5":
    
    print ("Ha salido")


else:
     print ("No ha elegido ninguna opción")
