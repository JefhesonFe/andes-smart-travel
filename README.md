# ANDES SMART TRAVEL — Avance 3

Prototipo **web responsive y funcional de demostración** basado en los mockups del Avance 2 del proyecto académico ANDES SMART TRAVEL (UTP, 2026).

## Requisitos
- Node.js 20.19+ o 22.12+
- Visual Studio Code
- Navegador moderno

## Abrir en Visual Studio Code
1. Descomprime `andes-smart-travel.zip`.
2. Abre la carpeta `andes-smart-travel` en Visual Studio Code (Archivo → Abrir carpeta).
3. En la terminal de VS Code ejecuta:
   ```bash
   npm install
   npm run dev
   ```
4. Abre en el navegador la dirección local que indique la terminal (normalmente http://localhost:5173).

## Pantallas incluidas
Bienvenida, registro, login, inicio, catálogo con filtros, ficha de servicio, comparación (hasta 3), favoritos, reserva, pago simulado, confirmación, historial de reservas, reseñas para servicios reservados, perfil, panel de proveedor y panel de administración.

## Probar los tres roles
En la pantalla **Iniciar sesión**, el bloque «Acceso rápido para presentación» ofrece botones **Turista**, **Proveedor** y **Administrador**. Estos accesos son exclusivamente demostrativos.

Prueba sugerida:
1. Entrar como Turista.
2. Buscar «Machu Picchu», abrir un tour, elegir fecha y número de personas.
3. Continuar a Pago y confirmar el pago **simulado**.
4. Abrir «Mis reservas», consultar la reserva y dejar una reseña desde el detalle del tour.
5. Salir, entrar como Proveedor, publicar o editar un servicio.
6. Salir, entrar como Administrador, ocultar/mostrar un servicio y moderar reseñas.

## Tecnologías y librerías
- **React** y **React DOM**: construcción de interfaces mediante componentes.
- **Vite**: servidor de desarrollo y compilación.
- **Lucide React**: iconografía de la interfaz.
- **CSS**: estilos responsive propios.
- **localStorage**: persistencia *local de demostración* en el navegador, sin backend.

## Limitaciones importantes
- **No existe backend ni conexión a PostgreSQL en esta versión**. Aunque el PDF define una arquitectura de tres capas y una base de datos de 17 tablas, este entregable es una implementación de interfaz navegable con lógica local de demostración.
- Los usuarios se guardan localmente y **las contraseñas de registro se almacenan sin protección real**. **Nunca utilices contraseñas reales ni información personal sensible**. No es apto para producción.
- Las reservas y pagos son simulados: **no hay cobros, validación externa de disponibilidad ni correos automáticos**.
- Se incluyen imágenes de referencia externas de Unsplash; se necesita conexión a internet para visualizarlas.
- Para alcanzar el sistema integral de tu alcance original debes implementar el backend, autorización segura por roles, sesiones, base de datos PostgreSQL, disponibilidad y reglas de negocio del marketplace.
- La comparativa permite seleccionar hasta 3 servicios, pero actualmente **no restringe a la misma categoría**; esta validación queda como mejora pendiente.
- El registro de proveedores y su estado son locales y demostrativos; no se verifica identidad/documentación.

## Estructura
```
andes-smart-travel/
├─ index.html
├─ package.json
├─ README.md
├─ .gitignore
└─ src/
   ├─ main.jsx
   ├─ App.jsx
   ├─ data.js
   └─ styles.css
```

## Git y GitHub
Después de abrir la carpeta en VS Code, puedes inicializar el repositorio:
```
git init
git add .
git commit -m "Avance 3: prototipo funcional de Andes Smart Travel"
```
Luego crea un repositorio en GitHub y sigue las instrucciones de la plataforma para enlazar `origin` y hacer `push`.

## Evidencias para el docente
Captura las pantallas de inicio, autenticación, catálogo, ficha, reserva, pago simulado, historial, panel proveedor y panel administrador. Adjunta `package.json`, estructura de archivos, historial de Git y evidencias de pruebas. No presentes el almacenamiento local como PostgreSQL ni el simulador como pasarela real.
