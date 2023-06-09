# 1er-Parcial-SPD

## 📋 Documentación. 
***
![Imagen no encontrada](./images/ArduinoTinkercad.jpg "Tinkercad")

 
## Proyecto: Montacargas Funcional. 

![Imagen no encontrada](./images/MontacargasFuncional.png "Parcial Nº1 SPD - UTN")

## Descripción.  
Es un modelo de montacarga funcional como maqueta para un hospital. Se implementa un sistema que pueda recibir ordenes de subir, bajar o pausar
desde diferentes pisos y muestra el estado actual del montacargas en el display 7 segmentos.


- **Funcionamiento del montacarga:** se implementa un algoritmo que permite que el elevador suba y baje o frene presionando los botones correspondientes.
   
- **Interfaz de usuario:** 3 botones, uno para subir pisos, otro para bajar pisos y otro para
detener el montacarga, 2 LEDS uno rojo que indica pausa y uno verde en movimiento.


## 🔗 Links.
***
```Enlace del proyecto en Tinkercad.```

- [Proyecto](https://www.tinkercad.com/things/d5WzS67z71N)

```Enlace al código del programa.```

- [Código](https://github.com/camilagargiulo/1er-Parcial-SPD/blob/main/codigo.txt)
## Funciones principales del programa: 

### _Cabe destacar las siguientes funciones del programa:_

- Esta funcion se encarga de leer las entradas digitales de los botones: botonSube, botonBaja y botonStop que son los #define que se utilizaron para agregar los pulsadores, asociandolos a pines de la placa arduino. Si la suma da distinta de 1 indica que cambio uno de los estados de los pulsadores.
 ~~~ C (Lenguaje del código)
int calcular_orden()
{
  int subir = digitalRead(botonSube)*2; 
  int bajar = digitalRead(botonBaja); 
  int stop = digitalRead(botonStop); 
  int orden = subir + bajar + stop; 
  return orden;
}
~~~
- A partir de la funcion anterior que arroja un entero, la siguiente funcion utiliza ese numero y define que comando debe seguir el programa, es decir, decodifica la orden emitida por el usuario al presionar uno de los botones; siendo 's' (subir) 'b' (bajar) o 'n' (no hacer nada o si esta en funcionamiento detener).
 ~~~ C (Lenguaje del código)
 char definir_comando(int orden)
{
  switch (orden)
  {
    case 3:
        comando = 's';
        break;
    case 2:
        comando = 'b';
        break;
    case 0:
        comando = 'n';
        break;
  }
  return comando;
}
~~~
***
##  **📚 Fuentes**

- [Tecnicatura Universitaria en Programación - UTN](http://www.sistemas-utnfra.com.ar/#/pages/carrera/tecnico-programacion/resumen)
- [Markdown-Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
***
 
