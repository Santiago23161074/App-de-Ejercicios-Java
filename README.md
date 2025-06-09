# App-de-Ejercicios-Java
# Pantalla de Inicio de Sesión en Android
Este proyecto es una aplicación básica de Android que presenta una pantalla de inicio de sesión. El usuario debe ingresar un correo electrónico válido y una contraseña específica para poder acceder al siguiente menú (MenuActivity).
---
## 🧩 Estructura del Proyecto
### activity_main.xml
- Diseño de la interfaz principal con los siguientes elementos:

- Imagen (Logo): en la parte superior (ImageView con @drawable/icono_inicio).

- Campo de correo electrónico (EditText con id Usuario_input).

- Campo de contraseña (EditText con id Contrasena_input).

- Botón de ingresar (Button con id Ingresar_btn).

- El fondo del layout es una imagen (@drawable/fondo_login) y se utiliza un diseño vertical centrado (LinearLayout dentro de un RelativeLayout).

### MainActivity.java
- Controlador lógico de la pantalla principal. Se encarga de:

- Validar el formato del correo electrónico usando la clase Patterns.

- Comparar la contraseña ingresada con una contraseña fija (tap*2025).

- Mostrar mensajes de error si los datos son incorrectos.

- Redirigir al usuario a la actividad MenuActivity si los datos son válidos.

### Validaciones implementadas:
- El correo debe tener un formato válido.

- La contraseña debe ser exactamente tap*2025.

- Si ambos son correctos, se realiza el cambio de actividad usando un Intent.

### 🚀 Requisitos
Android Studio

- SDK mínimo compatible con AppCompatActivity

- Una segunda actividad llamada MenuActivity (debe crearse para evitar errores al correr el proyecto)

- 🗂 Recursos necesarios (en carpeta res/drawable),fondo_login.png: Imagen de fondo para la pantalla de login.

- icono_inicio.png: Imagen o logo mostrado en la parte superior.

- courner.xml: Archivo para el diseño de fondo de los campos de texto (probablemente un shape con bordes redondeados).

### 📌 Notas adicionales
- El diseño está optimizado para centrarse en el contenido principal.

- La contraseña está codificada directamente en el archivo Java. Para mayor seguridad, en una app real debería usarse autenticación en servidor.

- El proyecto no incluye lógica en MenuActivity.java (el cual debes crear si deseas continuar el flujo).
## Vista
![Image](https://github.com/user-attachments/assets/7aa570fb-f621-473f-b5fc-58a5c3ad8f69)
---
# 📱Menu de Programas
Bienvenido al Visor de Programas 🎯, una aplicación Android que sirve como menú principal para acceder a diferentes ejercicios o módulos de práctica. Cada botón representa un ejercicio y permite navegar fácilmente entre las actividades.

## 📂 Estructura del Proyecto
- Este proyecto está compuesto por:

- Una actividad principal MenuActivity.java que actúa como menú.

- Un diseño visual en menu.xml con múltiples botones (CardView) que representan los ejercicios disponibles.

10 ejercicios separados, cada uno en su propia actividad (por ejemplo, Ejercicio1Activity, Ejercicio2Activity, etc.).

## 🚀 Funcionamiento
### 🔧 MenuActivity.java
- Esta es la actividad principal que se carga al iniciar la app.

- Se encarga de mostrar un menú de tarjetas (CardViews) donde cada una representa un ejercicio.

- Al hacer clic en una tarjeta, se lanza la actividad correspondiente al ejercicio usando Intent.

### 🔄 Cada botón está vinculado a un setOnClickListener, lo que permite la navegación rápida y dinámica:
```bash
  btnE1.setOnClickListener(v -> startActivity(new Intent(this, Ejercicio1Activity.class)));
```

🔚 El botón E11_btn está destinado a cerrar la sesión o salir del menú (usa finish()).

### 🧱 menu.xml
- Contiene un ScrollView con un LinearLayout vertical.

- Dentro se encuentran múltiples tarjetas (CardView) que contienen TextView con los nombres de los ejercicios.

- Hay una imagen en la parte superior (menu_icon) para embellecer la interfaz 🎨.

- Cada tarjeta tiene un diseño uniforme: márgenes, esquinas redondeadas, elevación y texto centrado.
---
# 🐶🐱🐭 Ejercicio1Activity – Visor de Programas 
Este módulo de la app Visor de Programas muestra una actividad interactiva donde el usuario puede seleccionar uno o varios animales de una lista de opciones (Perro, Gato y Ratón) mediante CheckBox ✅, ver su selección en pantalla 🧾 y limpiar o regresar al menú principal.

## 🧠 ¿Qué hace esta pantalla?
Esta actividad (Ejercicio1Activity) permite al usuario:

✅ Seleccionar uno o más animales: Perro 🐶, Gato 🐱, Ratón 🐭.

👁️ Ver en pantalla cuáles fueron seleccionados.

🧹 Limpiar las selecciones y el resultado.

🔙 Regresar al menú principal.

## 🚦 Lógica de funcionamiento
1. 🟢 onCreate(Bundle savedInstanceState)
- Se establece el contenido de la actividad (R.layout.ejercicio1) y el título: Ejercicio 1.

- Se enlazan los elementos del layout a sus respectivas variables.

2. ✅ Botón Aceptar
- Crea un mensaje con los animales seleccionados.

- Si ninguno está marcado, se muestra el mensaje:

- "No se seleccionó ningún animal."

- El mensaje final se muestra en el TextView lblResultado.

3. 🧹 Botón Vaciar
- Desmarca todas las CheckBox.

- Limpia el TextView de resultado.

4. 🔙 Botón Regreso
- Crea un Intent para volver a la actividad MenuActivity.

- Finaliza la actividad actual para evitar volver con el botón "Atrás".

---
# 📚 Ejercicio2Activity – Cálculo de Promedio 📊
Esta actividad forma parte de la aplicación Visor de Programas, y permite al usuario ingresar sus calificaciones trimestrales 📘📗📕 para calcular su promedio y saber si aprueba o reprueba la materia, mostrando el resultado de forma visual con texto y color. ✅❌

## 🎯 ¿Qué hace esta pantalla?
La actividad Ejercicio2Activity permite al usuario:

- 🧾 Ingresar tres notas (una por trimestre).

- 🧮 Calcular el promedio de esas notas.

- ✅ Mostrar si el estudiante aprobó o ❌ reprobó, con un cambio de color en el texto para reforzar el resultado.

- 🔙 Regresar a la pantalla anterior (con el botón de regresar).

## 🧱 Componentes de la interfaz
- Esta pantalla utiliza los siguientes elementos de interfaz:

- Tres campos de entrada (EditText) donde se escriben las notas del primer, segundo y tercer trimestre.

- Un TextView llamado lblNotaFinal que muestra el promedio calculado.

- Otro TextView llamado lblResultado que indica si el alumno aprobó o reprobó, con color verde o rojo respectivamente.

- Un botón (btnCalcular) que realiza el cálculo del promedio cuando se presiona.

- Y un botón (btnRegresar) que cierra esta actividad para volver a la anterior.

## ⚙️ Lógica de funcionamiento
- Cuando el usuario presiona el botón Calcular, se ejecuta lo siguiente:

- Se extraen los valores numéricos escritos en los tres campos de texto.

- Se convierten a double y se calcula el promedio: (pt + st + tt) / 3.0.

- El promedio calculado se muestra con dos decimales en lblNotaFinal.

- Luego se evalúa: Si el promedio es menor a 5.0, se muestra el texto "Reprobado" en color rojo.

- Si es igual o mayor a 5.0, se muestra "Aprobado" en color verde.

- Si hay algún error en la conversión (por ejemplo, si el usuario deja un campo vacío o escribe letras), se atrapa la excepción y se muestra:

- lblNotaFinal: "---"

- lblResultado: "Error en los datos" con color rojo.

## 💡 Consideraciones
- Las notas deben estar en formato numérico y pueden tener decimales.

- Se utiliza try-catch para evitar que la app se cierre si hay errores al ingresar los datos.

- Esta actividad no permite navegar directamente al menú principal, solo regresa a la actividad anterior.
---
# 🎯 Ejercicio3Activity – Selector de Color con RadioButtons 🎨
Esta actividad es parte de la aplicación Visor de Programas y permite al usuario seleccionar un color (Rojo, Verde o Azul) utilizando botones de opción (RadioButtons) y ver cuál ha sido elegido. También cuenta con un botón para regresar a la pantalla anterior.

## 🧠 ¿Qué hace esta pantalla?
- La actividad Ejercicio3Activity permite al usuario:

- Seleccionar un color entre tres opciones (Rojo, Verde o Azul) usando RadioButtons 🟥🟩🟦.

- Presionar el botón Aceptar para mostrar el color seleccionado.

- Ver el mensaje del color elegido o un mensaje de advertencia si no se seleccionó nada.

- Regresar a la pantalla anterior con el botón Regresar 🔙.

## 🧱 Componentes de la interfaz
- En la interfaz gráfica de esta actividad se utilizan los siguientes elementos:

- Un grupo de botones de opción (RadioGroup) que contiene tres RadioButtons:

- radioRed → opción para el color rojo.

- radioGreen → opción para el color verde.

- radioBlue → opción para el color azul.

- Un botón llamado buttonAceptar que el usuario presiona para confirmar su elección.

- Un TextView llamado textResultado que muestra el color elegido o un mensaje si no se seleccionó ninguno.

- Un botón llamado buttonRegresar que cierra esta pantalla y vuelve a la anterior.

## ⚙️ Lógica de funcionamiento
- Cuando se presiona el botón Aceptar:

- Se obtiene el id del botón seleccionado del grupo de RadioButtons.

- Si no se ha seleccionado ningún color (selectedId == -1), se muestra el mensaje:"No se ha seleccionado ningún color."

- Si se seleccionó un color:Se genera un mensaje con el color elegido, por ejemplo:
"Color elegido: Verde".

- El mensaje se muestra en el TextView textResultado, que se hace visible en ese momento.

Al presionar el botón Regresar, la actividad se cierra con finish() y el usuario vuelve a la pantalla anterior (probablemente el menú principal).

---
# 👥 Ejercicio4Activity – Lista de Nombres por Curso 🧑‍🏫📋
Esta actividad de la app Visor de Programas permite al usuario visualizar listas de nombres correspondientes a dos cursos distintos. Se puede seleccionar un nombre de la lista, vaciarla, o regresar a la pantalla principal.

## 🧠 ¿Qué hace esta pantalla?
- Ejercicio4Activity muestra una lista (ListView) con nombres de estudiantes. El usuario puede:

- Elegir entre dos cursos diferentes, cada uno con su propia lista de nombres.

- Ver el nombre que seleccionó desde la lista.

- Vaciar la lista completamente.

- Regresar a la pantalla anterior con el botón Regresar.

## 🧱 Componentes de la interfaz
- ListView lstNombres: Muestra la lista de nombres.

- TextView lblResultado: Muestra el nombre seleccionado.

- Button btnCurso1: Carga la lista del primer curso (Juan, María, Luis).

- Button btnCurso2: Carga la lista del segundo curso (Ana, Marta, Jose).

- Button btnVaciar: Vacía completamente la lista.

- Button btnRegresar: Cierra la actividad y vuelve a la pantalla principal.

## ⚙️ ¿Cómo funciona?
- Al iniciar, la lista está vacía. Se utiliza un ArrayList<String> (listaNombres) y un ArrayAdapter para enlazar los datos al ListView.

- Botón Curso 1: Llena la lista con los nombres Juan, María, Luis. Muestra el mensaje: "Selecciona un nombre" en el TextView.

- Botón Curso 2: Llena la lista con los nombres Ana, Marta, Jose. También muestra "Selecciona un nombre".

- Al seleccionar un nombre: Se actualiza el TextView (lblResultado) con el nombre seleccionado desde el ListView.

- Botón Vaciar: Limpia por completo la lista y muestra "Selecciona un nombre".

- Botón Regresar: Cierra esta pantalla y regresa a la anterior.
---
# 🔢 Ejercicio5Activity – Números Pares e Impares con Spinner 🎯
Esta actividad forma parte de la aplicación Visor de Programas y permite al usuario visualizar y seleccionar números pares o impares utilizando un Spinner (menú desplegable). También puede vaciar la lista o regresar a la pantalla anterior.

## 🧠 ¿Qué hace esta pantalla?
- La actividad Ejercicio5Activity permite al usuario:


- Mostrar una lista de números pares (del 0 al 10) o impares (del 1 al 9) presionando los botones correspondientes ➕➖.


- Visualizar el número seleccionado desde el Spinner en un TextView.


- Vaciar la lista y el resultado con el botón de limpiar.


- Regresar a la pantalla anterior con el botón Regresar.

##  🧱 Componentes de la interfaz

- En esta pantalla se utilizan los siguientes elementos:


- Un Spinner llamado spinnerNumeros que muestra una lista de números.


- Un TextView llamado tvResultado que muestra el número seleccionado por el usuario.


- Tres botones:btnPares → Carga los números pares del 0 al 10,btnImpares → Carga los números impares del 1 al 9,btnVaciar → Vacía la lista del Spinner y limpia el resultado.


- Un botón btnRegresar para volver a la pantalla anterior 🔙.

## ⚙️ Lógica de funcionamiento

- Al presionar el botón "Pares", se crea una lista de números pares desde el 0 hasta el 10, con formato "N° 0", "N° 2", ..., "N° 10", y se carga en el Spinner.


- Al presionar el botón "Impares", se genera una lista de impares desde el 1 hasta el 9 con el mismo formato y se muestra en el Spinner.


- Al seleccionar un elemento del Spinner, se actualiza el TextView tvResultado con el número seleccionado.


- Si se presiona "Vaciar", el Spinner se queda con una sola cadena vacía (para evitar errores) y se limpia el contenido del TextView.


- El botón "Regresar" simplemente cierra la actividad con finish() y devuelve al usuario a la pantalla anterior.
---
# 💰 Ejercicio6Activity – Cotizador de Servicios Extra 🧾🧮
Esta pantalla permite calcular el precio total de un producto con servicios opcionales adicionales, usando botones tipo Toggle para marcar lo que el cliente desea incluir.

## 🧠 ¿Qué hace esta pantalla?
Permite ingresar un precio base y seleccionar hasta tres servicios adicionales:

- 🛠 Instalación

- 👨‍🏫 Formación

- 🗃 Alimentación de Base de Datos

El sistema calcula el total a pagar en función de lo que el usuario haya seleccionado. También incluye un botón para regresar a la pantalla anterior.

## 🧱 Componentes de la interfaz
- EditText etPrecioBase: Entrada del precio base del producto.

- ToggleButton tbtnInstalacion: Activar/desactivar servicio de instalación.

- ToggleButton tbtnFormacion: Activar/desactivar servicio de formación.

- ToggleButton tbtnAlimentacionBD: Activar/desactivar servicio de alimentación de base de datos.

- TextView tvPrecioInstalacion: Precio del servicio de instalación.

- TextView tvPrecioFormacion: Precio del servicio de formación.

- TextView tvPrecioAlimentacionBD: Precio del servicio de alimentación de BD.

- TextView tvTotal: Resultado del precio total calculado.

- Button btnCalcular: Calcula el total con base en la selección.

- Button btnRegresar: Cierra esta actividad y vuelve a la anterior.

## ⚙️ ¿Cómo funciona?
- El usuario ingresa un precio base.

- Activa o desactiva servicios extra mediante botones ToggleButton.

- Pulsa el botón Calcular, y el sistema suma los costos adicionales seleccionados al precio base.

- El resultado aparece en tvTotal en formato moneda (XX.XX $).

- Si no se ha ingresado el precio base, se muestra un error en el campo.

## ⚠️ Manejo de errores
- Si el campo de precio base está vacío, aparece un mensaje de error solicitando que se llene.

- Si hay errores de formato (por ejemplo, texto en vez de números), el total mostrará "Error en los precios".

---
# 🔢 Ejercicio7Activity – Selector Numérico Personalizado 🎯
Esta pantalla permite al usuario seleccionar un número del 0 al 10 con pasos de 2 en 2 usando un componente NumberPicker. Además, muestra el número seleccionado en pantalla y permite regresar al menú anterior.

## 🎯 ¿Qué hace esta pantalla?
- Muestra una lista de valores posibles: 0, 2, 4, 6, 8, 10.

- Permite al usuario seleccionar uno.

- Muestra en un TextView el número actual seleccionado.

- Permite regresar al menú anterior mediante un botón.

## 🧱 Componentes de la interfaz
- NumberPicker numberPicker: Componente principal para seleccionar números.

- TextView txtValor: Muestra el número seleccionado.

- Button btnRegresar: Cierra la pantalla y regresa a la actividad anterior.

## ⚙️ ¿Cómo funciona?
- El NumberPicker es personalizado para mostrar únicamente valores entre 0 y 10, con un paso de 2.

- El arreglo displayedValues se llena con los valores permitidos: ["0", "2", "4", "6", "8", "10"].

- El valor inicial del selector es 4 (índice 2 del arreglo).

- Cada vez que se cambia el valor del selector, se actualiza el texto con el nuevo número.

- El botón Regresar cierra la actividad actual usando finish().
---
#💰 Ejercicio8Activity – Calculadora de Totales con IVA 🧾
Esta pantalla permite al usuario ingresar una cantidad de unidades y un precio unitario para calcular el total sin IVA y con IVA (16%). Se muestran los resultados y se valida que los datos ingresados sean válidos.

## 🎯 ¿Qué hace esta pantalla?
Recibe:

- Número de unidades.

- Precio por unidad.

Calcula:

- Total sin IVA.

- Total con IVA (16%).

- Muestra ambos resultados en pantalla.

- Incluye botón para volver al menú anterior.

## 🧱 Componentes de la interfaz
- EditText etUnidades: Campo para ingresar el número de unidades.

- EditText etPrecio: Campo para ingresar el precio por unidad.

- TextView tvTotalSinIva: Muestra el total sin aplicar IVA.

- TextView tvTotalConIva: Muestra el total incluyendo el IVA.

- Button btnCalcular: Ejecuta el cálculo.

- Button btnRegresar: Cierra la pantalla y regresa.

## ⚙️ ¿Cómo funciona?
- El usuario escribe las unidades y el precio unitario.

- Al presionar el botón Calcular, se multiplican ambos valores para obtener el total sin IVA.

- Se calcula el IVA (16%) y se suma al total.

- Se muestran ambos valores con 2 decimales.

- Si hay un error al ingresar los datos (campos vacíos o no numéricos), se muestra un Toast con un mensaje de advertencia.

---
# 👁️ Ejercicio9Activity – Control de Visibilidad de TextViews 🔘
Esta actividad permite ocultar y mostrar dos etiquetas de texto (TextView) por separado mediante botones específicos. Ideal para aprender a manipular la visibilidad de componentes en Android.

## 🎯 ¿Qué hace esta pantalla?
Muestra dos textos:

- Nombre

- Ciudad

- Permite ocultar o mostrar cada texto de manera independiente usando botones.

- También incluye un botón para regresar al menú anterior.

## 🧱 Componentes de la interfaz
- TextView lblnombre: Etiqueta que muestra un nombre.

- TextView lblciudad: Etiqueta que muestra una ciudad.

- Button btnon: Oculta el nombre.

- Button btnvn: Muestra el nombre.

- Button btnoc: Oculta la ciudad.

- Button btnvc: Muestra la ciudad.

- Button btnregresar: Regresa al menú anterior (cierra la actividad).

## 🧠 ¿Cómo funciona?
Cada botón tiene un setOnClickListener que cambia la visibilidad de los TextView usando:

```bash
setVisibility(View.GONE);     // Oculta el componente
setVisibility(View.VISIBLE);  // Lo muestra nuevamente
```
## 💡 Ejemplo de uso
- Se ve el nombre y la ciudad.

- Presionas Ocultar Nombre → desaparece el TextView del nombre.

- Presionas Mostrar Nombre → reaparece el nombre.

- Igual con la ciudad.

- Botón Regresar te lleva a la pantalla anterior.

---

# ➗ Ejercicio10Activity – División con validaciones y manejo de errores
Esta actividad permite realizar una división entre dos números, validando que no sean negativos ni cero, y mostrando un resultado claro. También se puede limpiar el formulario y regresar al menú anterior.

## 🎯 ¿Qué hace esta pantalla?
- Permite ingresar dos números A y B.

- Calcula y muestra el resultado de dividir A entre B.

- Evita divisiones inválidas:

- No permite dividir entre 0.

- No acepta valores negativos.

- Muestra advertencias si faltan datos o son incorrectos.

- Incluye botones para limpiar los datos o regresar.

## 🧱 Componentes de la interfaz
- EditText txtA: Campo de entrada para el número A.

- EditText txtB: Campo de entrada para el número B.

- TextView lblResultado: Muestra el resultado de la división.

- Button btnCalcular: Ejecuta la operación.

- Button btnVaciar: Limpia los campos y el resultado.

- Button btnRegresar: Cierra la actividad y regresa.

## 🧠 ¿Cómo funciona?
### 🔍 Validaciones incluidas:
- Campos vacíos: Se pide que se llenen ambos.

- Números negativos: No se permiten.

- División entre 0: Se muestra un mensaje de error.
---
# video
---
#  Autores
- Méndez García Ángel de Jesús
- Pérez Jiménez Santiago Enmanuel 
