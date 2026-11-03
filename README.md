# KILO

**El sistema para comercios con IA en todo.** Sacás una foto y se carga el producto. Sacás una foto a la factura del proveedor y se carga el stock. Le preguntás cómo vienen las ventas y te responde con tus datos.

Hecho en Palpalá, Jujuy. Ya está en producción.

- **Probalo en la web:** https://app.somoskilo.com
- **Bajalo en Android:** https://play.google.com/store/apps/details?id=com.kilo.app
- **Conocé más:** https://www.somoskilo.com

---

## El problema

Un comercio chico o mediano pierde horas en cosas que no venden: cargar productos a mano, pasar renglón por renglón la factura del proveedor, actualizar precios uno por uno y, al final del mes, no saber cuánto ganó de verdad.

Los sistemas que existen se pensaron para alguien que sabe de sistemas. El comerciante no tiene tiempo de aprenderlos.

## Qué hace KILO

- **Cobrar:** efectivo, tarjeta, QR y pagos mixtos, desde el celular o la compu.
- **Stock y productos:** con lector de código de barras, variantes y avisos de stock bajo.
- **Facturación electrónica de ARCA**, desde la misma caja.
- **Tienda online propia** para cada comercio, con su link y su QR.
- **Cajas, sucursales y equipo:** varias cajas, varios locales y permisos por persona.
- **Resultados:** ventas, gastos y ganancia real del negocio.

Sirve para cualquier rubro: almacenes, carnicerías, kioscos, verdulerías, ropa y más.

## La IA, en el día a día

| Lo que hace el comerciante | Lo que hace KILO |
|---|---|
| Le saca una foto a un producto | La IA propone nombre, categoría y datos, y el comerciante sólo confirma |
| Le saca una foto a la factura o a la lista de precios del proveedor | La IA lee cada renglón, lo encuentra entre sus productos y carga el stock o actualiza los precios |
| Le pregunta a Kilito «¿cómo vienen las ventas?» o «¿qué me falta reponer?» | Kilito responde con los datos reales de su negocio |
| Carga un producto nuevo | La IA le asigna la categoría sola |

La IA no es un chat agregado al costado. Está en las tareas que más tiempo le comen al comerciante.

## Tracción

- **Más de 100 usuarios.** Google Play muestra «100+ descargas» en la ficha pública de la app.
- La app está publicada en Google Play y en la web, y la usan comercios reales.

## Modelo de negocio

| Plan | Precio por mes | Para quién |
|---|---|---|
| Gratis | $0 | Ventas, productos y clientes ilimitados, 1 caja, tienda online y QR |
| Plus | $17.900 | Hasta 3 cajas, equipo, reportes de 12 meses y precios masivos |
| Pro | $39.900 | Hasta 3 sucursales, 10 cajas y 20 personas, con depósitos y auditoría |

Se paga con Mercado Pago o desde Google Play. El plan Gratis deja probar todo el día a día, y el comerciante pasa a Plus o Pro cuando el negocio crece.

## La decisión técnica que nos enorgullece

**Una IA que lee, pero nunca escribe.**

Kilito, el asistente, funciona con Claude Haiku 5.5. Para responder sólo puede usar tres herramientas de lectura: buscar productos, ver el stock bajo y ver el resumen de ventas. Cada consulta ve únicamente los datos de su propio comercio. El modelo no puede modificar nada.

Con las fotos pasa lo mismo: la IA propone y el comerciante confirma. No se guarda nada sin su visto bueno.

Además, el texto de los productos y de las facturas se trata como dato, nunca como instrucción. Así, un nombre de producto armado para engañar a la IA no puede hacerle hacer otra cosa.

Y lo cuidamos para que sea sostenible:

- Las instrucciones fijas quedan en caché, así que cada análisis de una foto cuesta una fracción de centavo de dólar.
- Cada plan tiene su propio cupo de uso de IA, y hay un techo diario global para que el gasto nunca se dispare.

## Cómo está hecho

- **App:** React 19 y TypeScript, con Vite y Mantine.
- **Android:** la misma app, empaquetada con Capacitor.
- **Servidor:** NestJS, Prisma, PostgreSQL y Redis.
- **IA:** Claude Haiku 5.5 para fotos, facturas y Kilito. Gemini para clasificar categorías.

## Sobre el código

KILO está en producción y maneja ventas y pagos de comercios reales, por eso el código es privado. Si el jurado quiere revisarlo, nos pide acceso por jujuy.dev y le damos permiso de lectura en el día.

## Equipo

- **Christian Gabriel Iturre Sandoval**, fundador de KILO. Palpalá, Jujuy.
- **Silvia Margarita Vidaurre**.

Hackatón Tren Solar · jujuy.dev · 2026
