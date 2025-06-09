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
