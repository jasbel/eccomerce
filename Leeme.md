# Análisis Funcional - Ecommerce "Del Productor al Consumidor"

## 💪 Objetivo General
Crear una plataforma de ecommerce que permita a pequeños productores vender directamente sus productos (ropa, inicialmente camisas y poleras) al consumidor final, sin intermediarios, mediante una experiencia de compra simple y digital.

---

## 🌟 Objetivos Específicos
- Mostrar productos disponibles con información clara (imagen, precio, tallas).
- Permitir realizar pedidos desde la plataforma.
- Gestionar pagos inicialmente mediante código QR.
- Confirmar pedidos a través de WhatsApp o formularios.
- Crear un backend que permita administrar productos y pedidos.
- Permitir escalar a métodos de pago más avanzados en el futuro (Stripe, Niubiz, etc).

---

## 👤 Usuarios del Sistema
### Cliente Final (Consumidor)
- Puede navegar por los productos.
- Seleccionar opciones de talla y cantidad.
- Iniciar un pedido y visualizar el QR de pago.
- Confirmar el pedido por WhatsApp o formulario.

### Administrador (Productor o Familiar)
- Puede agregar/editar productos.
- Ver pedidos realizados.
- Actualizar estado de los pedidos manualmente.
- Subir imágenes de productos.

---

## 🧰 Funcionalidades
### Productos
- Ver lista de productos.
- Ver detalles de un producto (nombre, descripción, imagen, precio, stock, tallas).
- Filtros (por talla, precio, etc) – futuro.

### Pedidos
- Seleccionar producto y talla.
- Elegir cantidad.
- Mostrar QR dinámico con el monto total.
- Confirmar pedido vía WhatsApp (mensaje prellenado).
- Registrar pedido en la base de datos.

### Confirmación
- Página que informa al usuario que debe enviar la captura del pago.
- Botón que abre WhatsApp con mensaje automático.

### Panel de Administración (privado)
- CRUD de productos.
- Ver lista de pedidos.
- Cambiar estado de pedidos (`pendiente`, `pagado`, `enviado`).

---

## 📊 Requisitos Técnicos
### Frontend
- **Astro** para generar un frontend estático, veloz y SEO-friendly.
- **TailwindCSS** para estilos rápidos y personalizables.
- Integración con el backend vía `fetch` o `API REST`.

### Backend
- **Node.js** + **Express** como API REST.
- **PostgreSQL** como base de datos relacional.
- **Prisma** (o Sequelize) como ORM.
- Generación de QR con `qrcode` o similar.
- Panel de administración con autenticación simple.

---

## 🔒 Seguridad y Privacidad
- Panel admin protegido por autenticación.
- No se almacenan datos sensibles de usuarios (por ahora no hay pagos en línea).
- Se recomienda capturar solo los datos mínimos necesarios: nombre, teléfono, pedido.

---

## 🔮 Escalabilidad Futura
- Agregar más categorías de productos.
- Incorporar usuarios con cuenta propia.
- Implementar pasarela de pagos.
- Control de stock automático.
- Notificaciones por correo o WhatsApp Business API.

---

## 📊 Métricas de Éxito
- Número de pedidos completados.
- Clientes recurrentes.
- Tiempo medio de atención por WhatsApp.
- Productos más vendidos.

