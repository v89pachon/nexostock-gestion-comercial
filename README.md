### NexoStock_Proyecto


# NexoStock — Gestión de pedidos, ventas e inventario

**Nombre de la aplicación:** NexoStock  
**Tipo:** prototipo web académico, ejecutable en navegador.  
**Idioma:** español.  
**Tecnologías:** HTML5, CSS3 y JavaScript (sin dependencias de servidor).

## Funcionalidades
- Panel principal con indicadores y alertas de inventario mínimo.
- CRUD básico de productos, búsqueda, desactivación y ajuste de existencias.
- Registro y edición de clientes.
- Creación, confirmación y cancelación de pedidos.
- Registro de ventas con validación de stock y descuento automático de inventario.
- Conversión de pedido a venta, con validación de disponibilidad.
- Reportes de ventas e inventario exportables a CSV.
- Exportación de copia de respaldo JSON.
- Usuarios/roles de demostración.
- Datos de ejemplo para probar la aplicación.

## Cómo ejecutar
1. Descarga o clona el repositorio.
2. Abre la carpeta `app`.
3. Abre `index.html` en un navegador actualizado (Chrome, Edge o Firefox).
4. La aplicación carga datos de demostración. Usa **Restablecer demo** para volver al estado inicial.

No necesita instalación de paquetes ni conexión a un servidor. La fuente tipográfica remota puede requerir Internet; si no está disponible, se usan fuentes de respaldo.

## Datos y limitaciones importantes
- Los datos se guardan en `localStorage` del navegador en el equipo donde se abre la aplicación. No se sincronizan entre dispositivos ni usuarios.
- Los perfiles de usuario son una simulación de interfaz, no un sistema de autenticación. No hay contraseñas ni control de acceso de seguridad real.
- No es apta para almacenar datos personales reales ni para operación comercial de producción.
- Antes de usarla en un negocio real, se requiere backend, base de datos, autenticación segura, autorización del lado servidor, copias de seguridad, pruebas de seguridad y revisión de protección de datos.
- La aplicación no integra facturación electrónica, pagos, contabilidad ni servicios externos.

## Reglas funcionales de la demo
1. Un pedido nuevo queda en estado `Pendiente` y no descuenta inventario.
2. Confirmar un pedido cambia su estado a `Confirmado`, pero no reserva existencias en esta versión.
3. Registrar una venta valida el stock disponible y descuenta las cantidades vendidas.
4. Convertir un pedido a venta vuelve a validar las existencias; si no alcanza el stock, no se registra la venta.
5. Un pedido pendiente o confirmado puede cancelarse; como el pedido no reserva inventario, la cancelación no requiere devolver unidades.
6. Los SKU deben ser únicos y no se permiten cantidades o existencias negativas.

## Estructura
```text
NexoStock_Proyecto/
├── app/
│   ├── index.html
│   ├── styles.css
│   └── app.js
├── documentos/
│   ├── Proyecto_NexoStock.docx
│   └── Proyecto_NexoStock.pdf
├── evidencias/
│   └── plan_pruebas.md
├── README.md
├── .gitignore
└── LICENSE
```


