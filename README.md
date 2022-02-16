# Codewars kata student correction IH

## Importante

Revisar el timezone porque hay desfase -> consola > Date.now()

## Intro

¿Estás cansado de tener que mirar a la pizarra para comprobar si tus alumnos han terminado la kata a tiempo? ¿Te apetece seguir flipando con la web de D3 en vez de girar el cuello hasta esa corta lista de estudiantes que han completado esa kata tan fácil? ¿Deseando que alguien haga el trabajo por tí? ¿Por programación?

Este código te cambiará la vida en este aspecto, del resto de tu vida ya te encargas tu. 

## Descripción

Este algoritmo permite comprobar el progreso de los alumnos y sus tiempos en codewars. Está compuesto por varios archivos CSV y unos ficheros de código en Python que harán todo el trabajo. 

## Instrucciones

### Carpeta input

Pide a tus alumnos que te hagan llegar sus usuarios de codewars. 
#### katas.csv
Encontrarás algo así. 
```
id,slug,date,minutes
54edbc7200b811e956000556,counting-sheep-dot-dot-dot,2020-10-20T12:00:00.000Z,180.0
57eae65a4321032ce000002d,fake-binary,2020-10-21T012:30:00.000Z,60.0
```
Solo deberás crear el contenido en función de las katas que hayas enviado, cuando las hayas enviado y el tiempo que les has dado para resolverla. 
La primera linea son los nombres de los campos de cada kata que envías. 
1. slug: La URL de una kata cualquiera es `https://www.codewars.com/kata/replace-with-alphabet-position/train/python`, su slug es `replace-with-alphabet-position`. 
2. date. Escrito en formato Datetime de la librería pandas
3. minutes. Cantidad de tiempo en minutos que tienen para resolver. 

NOTAS: 
1. Si se empieza el CSV con solo una kata, dará fallo, poned 2. 
2. Para incluir una kata nueva de la cual desconocemos el `slug`(nombre modificado que nos da la api y del cual tira el código para comprobar si las han hecho), insertar fila dejando el hueco de la columna `slug`, asi:
```59fa8e2646d8433ee200003f,,2022-02-16T12:30:00.000Z,120.0```


#### students.csv
Encontrarás algo así. 
```
name,username
Paula Postigo Rodrigo,paulapr
Almudena Gonzalez Salcedo,Almugs
Héctor Moreno Álvarez,hector-moreno
```
Solo deberás modificar el contenido para que corresponda con el nombre y el usuario de codewars de ese estudiante. 

### Carpeta source
Contiene un fichero `main.py` que resolverá todo. 


## API
```
# https://www.codewars.com/api/v1/users/Livia Canet/code-challenges/completed
```




