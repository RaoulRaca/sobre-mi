# 👨‍💻 Raoul Ramos — Desarrollador full-stack

Estudiante de **Ingeniería en Software** y fundador de
**[Raudex Systems](https://raudexsystems.com)**, empresa de software a medida con
sede en México.

Llevo **un año programando** y en ese tiempo he puesto **cuatro sistemas en
producción**: clínicas, consultorios y negocios que los usan todos los días. No
son proyectos de escuela ni demos — están en línea, con usuarios reales y datos
reales que no se pueden perder.

Aprendo construyendo cosas que tienen que funcionar.

---

## 🎓 Formación

- **Ingeniería en Software** — *en curso*
- **Universidad Popular Autónoma del Estado de Puebla (UPAEP)**
- Ingreso: **2025** · Egreso estimado: **2029**
- Programando desde **2025**

---

## 💻 Habilidades técnicas

**Lenguajes**
- TypeScript · JavaScript · Python · Java · SQL (PostgreSQL) · HTML · CSS

**Frontend**
- Next.js (App Router) · React · Tailwind CSS v4 · shadcn/ui · Framer Motion · Recharts

**Backend y datos**
- PostgreSQL con **Row Level Security** · Supabase (Auth + Postgres) · funciones RPC `SECURITY DEFINER`
- API Routes y Vercel Functions · integración con APIs de terceros (Resend, ESPN)

**Infraestructura y seguridad**
- Vercel (deploy, dominios, variables de entorno) · Git y GitHub
- Cabeceras CSP y HSTS · captcha invisible (Cloudflare Turnstile) · rate limiting · manejo de secretos en variables de entorno

**Arquitectura**
- Multi-tenancy con aislamiento a nivel base de datos · renderizado server-side y revalidación · diseño de esquemas con restricciones reales

---

## 🚀 Proyectos en producción

### VetSysCore — Sistema de gestión para clínicas veterinarias
🔗 [vetsyscore.com](https://vetsyscore.com)

Sistema completo de administración para clínicas veterinarias: expediente de
pacientes, agenda de citas y panel de métricas.

- **Stack:** Next.js (App Router) · TypeScript · Supabase · Tailwind · shadcn/ui
- **Detalles:** gráficas de actividad con Recharts, animaciones con Framer Motion, manejo de estado con Zustand, modo claro/oscuro.

### Ana Ramos Consultorio — Control de pacientes
🔗 [ana-ramos-consultorio.vercel.app](https://ana-ramos-consultorio.vercel.app)

Sistema de control de pacientes y agenda para consultorio médico, en uso real.

- **Stack:** Next.js · TypeScript · Supabase · Tailwind
- **Detalles:** formularios validados con React Hook Form, calendario de citas, reportes con Recharts.

### BarberCore — SaaS multi-tenant de citas
🔗 [barber-core.vercel.app](https://barber-core.vercel.app)

Plataforma donde cada dueño de barbería se registra, obtiene su panel privado y
su propio link público de reservas. **Un solo despliegue sirve a todos los
clientes**, con los datos aislados en la base de datos.

- **Stack:** Next.js · TypeScript · Supabase (PostgreSQL + RLS) · Tailwind v4
- **Reto técnico resuelto:** evitar la doble reserva de un mismo horario. En vez de validarlo en el frontend, lo resolví con un **índice único parcial** en Postgres — `(barber_id, fecha, hora) WHERE estado <> 'cancelada'` — y manejo del error `23505` en el cliente. La colisión es imposible a nivel base de datos, no solo improbable.
- **Aislamiento:** Row Level Security por `tenant_id` y funciones RPC `SECURITY DEFINER` para exponer la disponibilidad de horarios sin filtrar datos de otros clientes.

### Raudex Systems — Sitio corporativo con backend real
🔗 [raudexsystems.com](https://raudexsystems.com)

Sitio de la empresa, sin frameworks, con un backend de contacto funcional.

- **Stack:** HTML · CSS · JavaScript · Vercel Functions
- **Detalles:** formulario que envía correo real vía Resend con plantilla HTML propia, protegido con honeypot, rate limiting, restricción de CORS y captcha invisible de Cloudflare Turnstile verificado del lado del servidor. Cabeceras CSP y HSTS configuradas.

---

## 🛠️ Cómo trabajo

- **Las reglas van en la base de datos.** Si algo no debe pasar, lo impide un índice o una política de RLS — no una validación de JavaScript que se puede saltar.
- **Multi-tenant de verdad.** Un despliegue para todos los clientes, con los datos separados por políticas de seguridad a nivel de fila, no por filtros en el frontend.
- **Server-side por defecto.** App Router y revalidación; cero estado innecesario en el navegador.
- **Seguridad desde el día uno.** CSP, HSTS, captcha, rate limiting y secretos siempre en variables de entorno, nunca en el repositorio.
- **Software que se usa, no que se demuestra.** Cada proyecto de arriba está en línea y en manos de usuarios reales.

---

## 📫 Contacto

- 🌐 **[raudexsystems.com](https://raudexsystems.com)** — formulario de contacto directo
- 💼 GitHub: [@RaoulRaca](https://github.com/RaoulRaca)

---

<sub>Disponible para nuevos proyectos a través de Raudex Systems.</sub>
