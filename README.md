💼 Tarjeta de Presentación Responsiva con Jetpack Compose

Esta aplicación implementa una Tarjeta de Presentación digital (Business Card) en Android utilizando Jetpack Compose. Su característica principal es el diseño responsivo, que adapta completamente el layout de la tarjeta a la orientación o tamaño de la pantalla (móvil vs. tablet).

✨ Características Destacadas

Diseño Responsivo Dinámico: La función TarjetaPersonal utiliza BoxWithConstraints para detectar el ancho disponible (maxWidth) y renderizar automáticamente un diseño vertical (< 500.dp) o un diseño horizontal (>= 500.dp).

Interactividad con Intents: Los datos de contacto no son simples textos, sino botones funcionales (TextButton) que lanzan acciones nativas de Android:

📞 Teléfono: Llama al número (Intent.ACTION_DIAL).

📸 Instagram: Abre el perfil web (Intent.ACTION_VIEW).

📧 Email: Abre la aplicación de correo para enviar un nuevo email (Intent.ACTION_SEND).

Estilo Moderno: La foto de perfil se recorta en un círculo (.clip(CircleShape)).

Modularidad: El código está organizado en componentes Composable específicos (BotonNumeroVertical, BotonEmailHorizontal, etc.), facilitando el mantenimiento y la lectura.

📐 Estructura de los Layouts

Modo Vertical (Móvil)

Prioriza la información del perfil en la parte superior y apila los contactos en la parte inferior. Utiliza Image para el fondo.

Modo Horizontal (Tablet/Desktop)

Divide la pantalla para mostrar la información personal y los datos de contacto uno al lado del otro, aprovechando el espacio horizontal.

🚀 Uso del Componente

Para instanciar la tarjeta en tu MainActivity:

TarjetaPersonal(
    telefono = "333 333 333",
    pagina = "panchomalillos", // Instagram
    email = "panchomalilloss@gmail.com",
    nombre = "Francisco Malillos Castellano", // Usamos 'nombre' como en tu código original
    estudio = "Estudiante de ingeniería informática",
    instituto = "Universidad de Las Palmas de Gran Canaria",
    curso = "4º Curso",
    ciudad = "Las Palmas de Gran Canaria"
)


Nota: Se requiere tener imágenes llamadas descarga, telefono, instanuevo__1_, email, y fondotp2 en la carpeta res/drawable de tu proyecto para que compile correctamente.
