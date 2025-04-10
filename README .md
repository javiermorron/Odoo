
# Odoo: Guía Completa para Desarrolladores y Empresas

Bienvenido al repositorio donde comparto herramientas, tips y automatizaciones para trabajar con Odoo sin perder tiempo. Esta guía está pensada para quienes quieren entender qué es Odoo, cómo instalarlo, probarlo y empezar a desarrollar módulos propios.

---

## 📄 ¿Qué es Odoo?

Odoo es un software ERP (**Enterprise Resource Planning**) que permite centralizar la gestión de todas las áreas de una empresa: ventas, compras, inventario, contabilidad, recursos humanos, mantenimiento y mucho más.

Cuenta con:
- Una versión **Community** (código abierto - LGPLv3)
- Una versión **Enterprise** (licencia comercial con funcionalidades extendidas)

![odoo modulos](https://github.com/javierma73/Odoo/blob/main/odoo%20modulos.png)

---

## 🔧 Modo desarrollador en un clic

La extensión para navegadores “Odoo Debug” activa el modo desarrollador rápidamente:

- [Para Google Chrome](https://chrome.google.com/webstore/detail/odoo-debug/hmdmhilocobgohohpdpolmibjklfgkbi)
- [Para Mozilla Firefox](https://addons.mozilla.org/es/firefox/addon/odoo-debug)

Haz clic en el 🐵 para activar el modo desarrollador, y doble clic para activar con assets.

---

## 🪖 Instalación de Odoo en Windows (modo desarrollador)

Recomendada para desarrollar y correr varias versiones de Odoo:

### Clona el repositorio
```bash
C:\> git clone https://github.com/odoo/odoo.git
```

### Verifica Python y pip
```bash
C:\> python --version
C:\> pip --version
```

### Instala PostgreSQL
[Descargar PostgreSQL](https://www.postgresql.org/download/windows/)

- Crea un usuario que no sea "postgres"
- Dale permisos para crear base de datos desde pgAdmin

---

## 📦 Crea un entorno virtual con Python

Instalá virtualenv:
```bash
pip install virtualenv
```

[Guía rápida para entornos virtuales](https://github.com/javierma73/Entornos-virtuales/blob/main/Entornos-virtuales.md)

---

## 🎮 ¿Querés probar Odoo ya mismo?

Podés usar estas demos online:
- [Trial oficial de Odoo](https://www.odoo.com/es_ES/trial)
- [Odoo en línea](https://www.odoo.com/documentation/13.0/administration/install/install.html#online)

---

## 🪓 Comparación de Ediciones

| Característica       | Community | Enterprise | Online | SH |
|------------------------|-----------|------------|--------|----|
| Licencia               | LGPLv3    | Comercial  | SaaS   | Comercial |
| Soporte oficial        | No        | Sí         | Sí     | Sí |
| Personalización        | Alta      | Alta       | Baja   | Alta |
| Acceso al código       | Completo  | Completo   | No     | Completo |

Más info: [Odoo Editions](https://www.odoo.com/es_ES/page/editions)  
Planes: [Precios](https://www.odoo.com/es_ES/pricing-plan)

![Precios y Planes](https://github.com/javierma73/Odoo/blob/main/Precios%20Mensual%20de%20Odoo.png)

---

## 🌐 Configuración de Entorno de Desarrollo

Podés instalar Odoo manualmente o usar Docker. La imagen oficial está aquí:
[Docker Hub - Odoo](https://hub.docker.com/_/odoo)

### Requisitos:
- Python ≥ 3.6
- PostgreSQL
- Librerías de dependencias (según versión de Odoo)

---

## 🏆 Tu primer módulo

Un módulo en Odoo se estructura en un directorio con:

- `__init__.py`
- `__manifest__.py`
- Carpetas: `models/`, `views/`, `data/`, `controllers/`

Tutorial oficial: [Su primer módulo](https://www.odoo.com/documentation/15.0/es/administration/odoo_sh/getting_started/first_module.html#your-first-module)

---

📆 Actualización en progreso...
Este README crecerá con ejemplos reales, scripts de automatización y módulos que uso con clientes reales.

---

**Javier Morrón**  
*IA, automatización y propósito: ese es mi lenguaje.*
