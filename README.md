# 💼 Tarjeta de Presentación Responsiva (Jetpack Compose)

Este proyecto desarrolla una Tarjeta de Presentación digital (Business Card) en Android utilizando **Jetpack Compose**. La funcionalidad central es el **diseño responsivo**, que adapta automáticamente la interfaz de usuario a la orientación y al tamaño de la pantalla.

---

## ✨ Características Destacadas

* **Diseño Adaptativo con BoxWithConstraints:**
    * La función `TarjetaPersonal` evalúa el ancho de la pantalla (`maxWidth`).
    * Cambia el layout entre el modo **Vertical** (para móviles) y **Horizontal** (para tablets o pantallas anchas) de forma dinámica.
* **Interactividad y Manejo de Intents:** Los botones de contacto lanzan acciones nativas de Android, haciendo la tarjeta totalmente funcional:
    * 📞 **Teléfono:** Utiliza `Intent.ACTION_DIAL` para iniciar una llamada.
    * 📸 **Instagram:** Utiliza `Intent.ACTION_VIEW` para abrir el perfil en el navegador.
    * 📧 **Email:** Utiliza `Intent.ACTION_SEND` para abrir el cliente de correo.
* **Estilo UI/UX:**
    * Uso de `CircleShape` para la foto de perfil.
    * Enlaces de contacto visualmente resaltados (subrayados y de color azul).

---

## 📐 Estructura de Componentes

| Componente | Uso Principal |
| :--- | :--- |
| `TarjetaPersonalVertical` | Layout apilado, optimizado para la orientación vertical o pantallas pequeñas. |
| `TarjetaPersonalHorizontal` | Layout dividido en secciones, optimizado para la orientación horizontal o pantallas grandes. |
| `Boton...` (Varios) | Encapsulan la lógica del `TextButton` y el lanzamiento del `Intent` asociado. |

---

## 🚀 Uso del Componente

Simplemente llama al componente principal en tu `MainActivity` e inyecta los datos:

```kotlin
TarjetaPersonal(
    telefono = "333 333 333",
    pagina = "panchomalillos", 
    email = "panchomalilloss@gmail.com",
    name = "Francisco Malillos Castellano", 
    estudio = "Estudiante de ingeniería informática",
    instituto = "Universidad de Las Palmas de Gran Canaria",
    curso = "4º Curso",
    ciudad = "Las Palmas de Gran Canaria"
)
```
Nota: Para que el proyecto compile, asegúrate de que todas las imágenes referenciadas (descarga, telefono, instanuevo__1_, email, fondotp2) se encuentren en la carpeta res/drawable.
