# --- GUÍA DE ARQUITECTURA ---

# Proyecto desarrollado en Python, en orientación a objetos. He priorizado la legibilidad del código y la separación de responsabilidades para facilitar el mantenimiento futuro.

# ------------------------------------------------------

# Estructura de Clases: utilizo un patrón de herencia para los tipos de alquileres.

# Vehiculo: atributos comunes (matrícula, marca, precio base) y el método 'calcular_precio()'

# VehiculoPorDias: hereda de 'Vehiculo' y añado dias de alquiler, he sobreescrito el metodo de calcular precio para multiplicar el precio base por los días.

# VehiculoPremium: hereda de 'Vehiculo' y guardo los datos en un diccionario ('extras'), sobreescribo calcular_precio() para sumarle ese extra al precio base.

# -- Excepciones --
# He creado la clase 'PrecioInvalidoError' heredado de 'Exception' como un sistema de control de errores, permite evitar precios o días negativos sin romperse.

# ------- LÓGICA --------

# main -> controlado por un bucle while, este actúa como controlador principal mostrando un menú interactivo en la consola

# Estructura de datos -> el inventario se almacena en la memoria durante la ejecución usando un diccionario (vehiculos)

# clave -> la matricula del vehiculo debe ser unica
# valor -> la instancia del objeto, que es el vehículo

# La entrada del usuario está controlada por un try/except para un control de errores.

# He utilizado una programación orientada a objetos por la facilidad que da a lo largo, si en un futuro necesitas añadir otra clase, simplemente debemos hacer que herede a 'Vehiculo' sin tener que modificar demasiado el código.
