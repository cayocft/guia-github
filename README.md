# GUÍA BÁSICA DE GIT  

## Índice    
1. [Primeros Pasos](#id1)
2. [Crear Repositorio en GitHub](#id2)
3. [Iniciar Git y subir su primer proyecto a GitHub](#id3)
4. [Actualizar Repositorio](#id4)
5. [Trabajar con versiones](#id5)
## 1. Primeros Pasos<a name="id1"></a>  
Crear una cuenta en GIthub 
</br>
Deben primero indicar quien es el que utilizará y modificará los proyectos de Git. Así GitHub podrá determinar que usuario realizo un cambio en el proyecto.
Para esto deberán indicar su nombre y su correo electrónico (el correo debe estar registrado en GitHub)
</br>
Deberán indicar su nombre

```
git config --global user.name "Juanito Perez"
```
Luego indicar su correo que usan en GutHub
```
git config --global user.email juanito.perez@gmail.com
```
Los Comandos anterirores se registraràn de manera global en su Sistema Operativo

## 2. Crear Repositorio en GitHub <a name="id2"></a>  
Deberán ingresar con su cuenta en GitHub y en el menú de su perfil ingresar a Repositorios y seguidamente precionar el botón "New" que se encuentra en la parte superior de esa página

## 3. Iniciar Git y subir su primer proyecto a GitHub <a name="id3"></a>  

En el directorio que se encuentre su proyecto (dentro de una carpeta raíz) deberán iniciar su repositorio
```
git init
```
Luego, agregar los cambios al entorno "ensayo". Inicialmente agregará todos los directorios a este entorno. 

```
git add .
```
Luego deberán capturar una instancia del proyecto preparado "que se encuentra en su etorno de ensayo". Esto se hace con el siguiente comando (-m: indica que ingresaran un comentario de su captura de instancia):
```
git commit -m " comentario de esta instancia"
```

Luego, deberàn indicaer cual es su repositorio remoto donde enviaran todo los cambios preparados con los comandos anteriores:
```
git remote add origin https://github.com/cayocft/prueba.git
```
El link es el repositorio que ustedes crearon en el punto ` "Crear Repositorio en GitHub" `

Por último, subiran todos los cambios de su proyecto previamente preparado (con los comandos ejecutados anteriormente) a su repositorio remoto creado anteriormente.
```
git push -u origin master
```
Esto creará una rama máster (rama por defecto) en su repositorio en la que se encuentra todo el proyecto recientemente subido

## Actualizar Repositorio <a name="id4"></a>

Cuando estes trabajando en tu proyecto y necesitas subir los cambios (a la rama raíz) deben aplicar algunos comandos del punto "3". Por lo que deberán agregar los cambios al entorno de ensayo, capturar su nueva instancia del proyecto a actualizar y por último subir la instancia preparada al rempositorio remoto
```
git add .
```
```
git commit -m "nueva version del proyecto actualizado"
```
```
git push -u origin master
```
`master` es su rama raíz que se encuentra en su repositorio local

## Trabajar con Versiones <a name="id5"></a>
Para trabajar con versiones sin alterar la rama raíz de su proyecto (Esto evita que su proyecto sufra cambios que tengan errores durante la codificación) se recomienda crear una rama nueva (versión) que contendra una copia exacta de su rama raíz `master`
</br>
Para crear una rama nueva deberán ejecutar dentro de la raíz de su proyecto (carpeta):
```
git checkout -b nombre_de_la_rama
```
Lo anterior creará y se posicionará en la rama creada
</br>
Una vez hecho esto, podras trabajar en tu proyecto sin alterar el proyecto raíz. Cuando ya estes listo para subir los cambios a tu proyecto y combinarlos con tu rama raiz. Deberás ejecutar:
```
git add .
```
```
git commit -m "nuevos cambios a mi nueva rama"
```
```
git push -u origin nombre_de_la_rama
```
Luego. Deberán dirigirse a su repositorio loca y aparecerá una alerta.....