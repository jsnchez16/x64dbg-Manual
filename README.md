# ✖6️⃣4️⃣dbg - Manual

---
---

Cheatsheet operativo de x64dbg para análisis y explotación de binarios Windows.

---
---

**x64dbg** es una herramienta de ingeniería inversa para el análisis estático y dinámico en Windows de binarios ejecutables de 32 y 64 bits.

Este depurador gráfico open source permite el uso de breakpoints, inspección de registros, ver y modificar memoria, trazar instrucciones y analizar llamadas al sistema o librerías externas.

---

## ⚙️ ***1. Instalación***

- [Página oficial](https://x64dbg.com/)
- [Repositorio de GitHub](https://github.com/x64dbg/x64dbg)
- [Descarga desde Sourceforge](https://sourceforge.net/projects/x64dbg/files/snapshots/)

Desde Sourceforge seleccional la snapshot más reciente que tenga el mayor número de descargas.

---

<img width="948" height="778" alt="image" src="https://github.com/user-attachments/assets/b476f387-bd4e-463a-befb-917169625b2f" />

---

Tras unos segundos se iniciará la descarga de un .zip . En la carpeta de descarga del .zip descomprimirlo.

Abrir la carpeta descomprimida y seleccionar la subcarpeta '_release_' . En esta carpeta se encuentran los ejecutables del programa para las diferentes arquitecturas.

---

<img width="538" height="447" alt="image" src="https://github.com/user-attachments/assets/c02591d1-4ad6-4113-b0dc-ed8cf374d435" />

---

Existen dos opciones para el programa.

- x32\x32dbg.exe para depurar un ejecutable de 32 bits.
- x64\x64dbg.exe para depurar un ejecutable de 64 bits.
- También se puede ejecutar x96dbg.exe y seleccionar la arquitectura allí.

Para mayor comodidad se pueden crear accesos directos. De ahora en adelante se trabajará con la opción de x32dbg, aunque la versión x64 es igual.

**Es necesario lanzar el programa como administrador.**

Es posible que al ejecutar el programa salte un aviso de '_Windows protegió su PC_'. Basta con hacer clic en '_Más información_'.

---

<img width="518" height="469" alt="image" src="https://github.com/user-attachments/assets/a40ad5e9-7866-4fbc-a2f9-6e89bded4c5c" />

---

Y seleccionar ejecutar de todas formas.

---

<img width="515" height="475" alt="image" src="https://github.com/user-attachments/assets/a395a126-eab5-4dad-afc5-c2b492df9604" />

---

Con esto ya se iniciará en este caso x32dbg.

---

<img width="1271" height="1271" alt="image" src="https://github.com/user-attachments/assets/7aca22eb-5ebd-4622-854a-d0f5a2d3af43" />

---

## ***2. Uso***

* **2.1 Selección del binario a analizar.**
  
  -  En la barra superior de herramientras Archivo -> Abrir -> Seleccionar el binario vulnerable.

---

<img width="1276" height="1275" alt="image" src="https://github.com/user-attachments/assets/80ffa764-3ecd-49c8-8911-c6e0f4cce970" />

---

A partir de este momento, el binario se ejecuta y pasa al estado 'Pausado'.

---

<img width="67" height="34" alt="image" src="https://github.com/user-attachments/assets/12745800-9e73-4d27-be43-06ba58835dcc" />

---

La siguiente barra de herramientas que aparece arriba se corresponde con la ejecución del programa.

---

<img width="669" height="29" alt="image" src="https://github.com/user-attachments/assets/0ee02aa4-8ea9-4db4-bbf4-b7d7a1efa8bf" />

---

* **2.2 Vistas**

Justo debajo, se encuentran las diferentes vistas que ofrece x64dbg.

* **2.2.1 Vista de CPU**

La vista principal corresponde a la vista de CPU, principalmente se encuentra, de izquierda a derecha, la dirección a la que corresponde cada instrucción, código en hexadecimal, vista del código ensamblador del binario y comentarios. A la derecha del código ensamblador también aparece la información actual que se almacena en los registros y que irá cambiando comforme avance la ejecución.

Desde aquí además es posible establecer los puntos de ruptura para la depuración del binario.

Añadir comentarios en las secciones del código es posible y ayuda a analizar mejor la ejecución.

---

<img width="1091" height="658" alt="image" src="https://github.com/user-attachments/assets/ca0e635a-076e-4dea-b9b1-c2d253e8af40" />

---

<img width="440" height="134" alt="image" src="https://github.com/user-attachments/assets/4349ae3d-b6ec-445f-9ccb-c4a17930744c" />


---

<img width="1279" height="812" alt="image" src="https://github.com/user-attachments/assets/25d511a4-b880-4639-adf9-edd38a35d929" />

---

La vista Logs presentan la información de todo lo que va ocurriendo durante la ejecución.

---

<img width="782" height="552" alt="image" src="https://github.com/user-attachments/assets/648afe13-dcae-4350-9adb-1860746c2aa1" />

---

Otras vistas interesantes como la vista Breakpoints, Mapa de memoria y Pila de llamadas ofrecen información importante sobre el estado de ejecución del binario.

---

En la barra de herramientas principal, Opciones -> Preferencias se pueden seleccionar diferentes aspectos de la ejecución como por ejemplo el que viene activado por defecto para que el programa se detenga en el punto de entrada al iniciar.

---

<img width="455" height="573" alt="image" src="https://github.com/user-attachments/assets/90e7a947-ad82-43c7-b2a4-62773c2b52fd" />

---

En Opciones -> Apariencia se muestran todas las posibilidades de apariencia de las vistas para que sea más sencillo trabajar con el programa

---

<img width="544" height="475" alt="image" src="https://github.com/user-attachments/assets/f5d3d1a1-d185-4e58-a82d-fdf3873032f3" />

---

* **2.2.2. Gráfico**

Al seleccionar varias secciones del código es posible abrir un gráfico del flujo de ejecución del programa.

---

<img width="1264" height="613" alt="image" src="https://github.com/user-attachments/assets/2e392f18-6dc6-4092-962f-27bf8deeb690" />

---

Lo que se obtiene es similar a la vista en otros programas como IDA y permite entender mejor el flujo de ejecución.

---

<img width="592" height="738" alt="image" src="https://github.com/user-attachments/assets/1ec6c756-6128-469d-a510-496ef906ad7e" />

---

Si en preferencias en la pestaña GUI marcamos la opción 'Show RVA addresses in graph view' esto muestra las direcciones donde se encuentran las instrucciones cuando estamos en modo de vista de gráfico.

---

<img width="462" height="576" alt="image" src="https://github.com/user-attachments/assets/0ecb0ac9-5240-46e8-be08-dbde3b708304" />

---

<img width="549" height="464" alt="image" src="https://github.com/user-attachments/assets/55700ec3-a1cd-465a-b6db-bc00ebc82ac2" />




