## SOLUCION

# PASO 1

crear archivo de configuracion para nginx, nginx.conf

# PASO 2

copiar el archivo nginx.conf al contendero, hacerlo en el dockerfile

COPY nginx.conf /etc/nginx/conf.d/default.conf

Compilar y ejecutar

:)