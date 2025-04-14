🧩 Diseño de Software con MVC – Ejemplo: Aplicación ToDo

A continuación se describe un ejemplo completo del proceso de diseño de software para una aplicación de lista de tareas (**ToDo App**), aplicando cada uno de los pasos del ciclo de diseño y usando el patrón **Modelo–Vista–Controlador (MVC)**.

---

## 🎨 Tipos de Diseño

### 1. Diseño de Interfaz (UI/UX)
Diseñaremos una interfaz simple y clara, donde el usuario pueda:
- Ver una lista de tareas.
- Agregar nuevas tareas.
- Marcar tareas como completadas.
- Eliminar tareas.

Nos enfocaremos en que la experiencia sea intuitiva, accesible y funcional tanto en computadora como en móvil.

### 2. Diseño Técnico (estructura del software)
Utilizaremos el patrón **MVC** para organizar el código:
- **Modelo**: gestiona las tareas (crear, leer, actualizar, eliminar).
- **Vista**: muestra la interfaz al usuario.
- **Controlador**: recibe acciones del usuario y comunica la vista con el modelo.

### 3. Diseño de Datos
Cada tarea estará representada por un diccionario o una fila de base de datos con:
- ID
- Descripción
- Estado (pendiente o completada)
- Fecha de creación

---

## 🏗️ Definición de la Arquitectura

### 4. Estructura General del Sistema
Aplicación de arquitectura **monolítica** pequeña y simple, ideal para este proyecto, pero organizada con MVC para permitir su crecimiento.

### 5. Tipo de Arquitectura
Usaremos una arquitectura **cliente-servidor**, donde el cliente (navegador) se conecta a un servidor backend que gestiona las tareas.

### 6. Importancia de la arquitectura
MVC permite:
- Separación clara de responsabilidades.
- Escalabilidad si en el futuro queremos usar base de datos o una API.
- Facilita que varias personas trabajen simultáneamente (diseñador UI, backend, etc.).

---

## 🖌️ Diseño de Interfaces

### 7. Bocetos y prototipos
Crearemos bocetos de las pantallas:
- Pantalla principal con la lista de tareas y botones de acción.
- Formulario para agregar nueva tarea.

### 8. Herramientas
Usaremos **draw.io** para los diagramas y bocetos iniciales, por ser gratuito, colaborativo y fácil de usar.

---

## 🧩 Creación de Diagramas

### 9. Tipos de Diagramas
- **Flujo**: cómo se procesa una nueva tarea.
- **Casos de uso**: "el usuario crea una tarea", "el usuario completa una tarea".
- **Clases**: si usamos orientación a objetos.
- **Componentes**: vista, modelo y controlador separados.

---

## 🧠 Definir Algoritmos

### 10. Pensar antes de programar
Por ejemplo:
- Si el usuario marca una tarea como completada, debemos actualizar su estado en el modelo y refrescar la vista.

### 11. Herramientas
- Usaremos **pseudocódigo** para escribir la lógica de agregar y borrar tareas.
- **Diagrama de flujo** para representar la navegación del usuario.

---

## ⚙️ Seleccionar Tecnologías

### 12. Herramientas que utilizaremos
- **Lenguaje**: Python
- **Framework web**: Flask
- **Frontend**: HTML + CSS + JavaScript (básico)
- **Base de datos**: SQLite (opcional para persistencia)

### 13. Criterios
- El equipo tiene experiencia con Python.
- Flask es ligero y permite estructurar con MVC fácilmente.
- HTML/CSS son suficientes para el prototipo.

---

## 📋 Especificaciones Técnicas

### 14. Módulos del sistema
- **Modelo**:
  - Clase o módulo `Tarea` con atributos: `id`, `descripcion`, `completada`.
  - Métodos: `crear_tarea()`, `listar_tareas()`, `marcar_completada()`, `eliminar_tarea()`.

- **Vista**:
  - Plantilla HTML que muestra la lista y botones de acción.

- **Controlador**:
  - Funciones en Flask que reciben los clics del usuario y llaman al modelo, luego redirigen a la vista.

### Entradas/Salidas esperadas
- Entrada: texto de la tarea nueva.
- Salida: visualización actualizada en pantalla.
- Excepciones: si el texto está vacío, mostrar advertencia.

---
