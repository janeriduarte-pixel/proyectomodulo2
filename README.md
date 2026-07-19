# proyectomodulo2

Para ingresar como usuario: profe@alke.com clave: 1234


En el Login (index.html): Usamos el esqueleto de HTML:5 esto le dice al navegador que ahí­ va un formulario que necesita recopilar datos de acceso con validaciones nativas.
En el Menú (menu.html): Estructuramos la tabla usando, (para los títulos: Detalle, Fecha, Monto) y dejamos el cuerpo de la tabla con un id="transaction-history" completamente vacío para que JavaScript pudiera llenarlo después.
Colores y Fondos: Usamos estilos en bloque para pintar el fondo de la pantalla de un gris muy suave (#f4f7f6) que no canse la vista.
La Tarjeta de Saldo: Creamos la clase .balance-card con un degradado moderno (linear-gradient) entre dos tonos de azul para que resalte y parezca una tarjeta de crédito premium o la pantalla de un banco real.
Diseño para Celulares: Usamos el sistema de filas (row) y columnas (col-md-6, col-md-5) para indicarle a la pantalla de donde se usa la pagina, si es por computadora o celular para apilar información.
La Barra de Navegación: Usamos la clase .navbar-expand-lg y el botón .navbar-toggler. Esto hace que el menú de arriba se guarde automáticamente dentro de un botón 🟰 (las tres rayitas) cuando se abre en pantallas pequeñas.
El Formulario Flotante: En lugar de crear otra página entera para los depósitos, usamos el componente modal de Bootstrap. Al presionar "+ Depositar / Retirar", la pantalla del menú se oscurece y flota una ventana limpia para meter el monto.
Cálculos Financieros: se está usando JavaScript para cuando el usuario digita un monto, este se encarga de transformar ese texto en un número entero (parseInt()). Luego evalúa: si elegiste "depositar", hace una suma; si elegiste "retirar", hace una resta.
Estructura de Datos: Para la mejora del historial, usamos Objetos de JavaScript. Cada movimiento se empaqueta así: { detalle: '...', fecha: '...', monto: ..., tipo: '...' }.
Captura de Eventos: Reemplazamos el clásico y aburrido código de JS por el selector de jQuery $('#btn-process-funds').click(...) para reaccionar al instante cuando el usuario presiona un botón.
Escribir HTML sobre la marcha: Usamos el método $('#transaction-history').append(...). Esto toma el objeto del movimiento y "fabrica" una nueva fila ... con etiquetas de Bootstrap directo en la tabla sin necesidad de recargar la página.
Animaciones: Usamos .fadeIn(), .slideDown() y .delay(2000).slideUp() para que los mensajes de error o las alertas de "Transferencia exitosa" aparezcan y desaparezcan con un efecto suave y agradable a la vista.
Buscador Inteligente: Con el evento $('#search-contact').on('input', ...) escuchamos cada letra que el usuario teclea, revisamos nuestra lista y mostramos las sugerencias al vuelo.
Persistencia: Al usar localStorage.setItem('balance', nuevoSaldo), guardamos el dinero directamente en la memoria interna del navegador.
Compartir Información: Cuando pasamos de la pantalla de transferencias al menú, el menú ejecuta un localStorage.getItem('balance') y localStorage.getItem('globalTransactions'). Así logra enterarse de cuánto dinero nos queda y qué transferencias hicimos en la otra pantalla, manteniéndose todo sincronizado.
