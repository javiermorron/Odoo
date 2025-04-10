# ¿Qué es Odoo y para qué sirve?

Odoo es un software ERP (**Enterprise Resource Planning**) es un sistema de planificación de recursos empresariales.

Se trata de una solución que permite centralizar toda la gestión de la empresa agilizado tareas y controlando eficazmente las diferentes áreas.. Cuenta con una versión "comunitaria" de código abierto bajo licencia LGPLv3 y una versión empresarial bajo licencia comercial que complementa la edición comunitaria con características y servicios comerciales y desarrollada por la empresa belga Odoo S.A.

Ofrece una amplia variedad de módulos integrados, que incluyen diferentes áreas de la empresa como son: ventas, compras, inventario, contabilidad, recursos humanos, mantenimiento y más. Se centra en la modularidad y la flexibilidad, permitiendo a las empresas personalizar y adaptar el software según sus necesidades específicas, por lo que algo importante del sistema es que se adapta mayormente a tu operación y no necesariamente tu empresa debe adaptarse al sistema.

![odoo modulos](https://github.com/javierma73/Odoo/blob/main/odoo%20modulos.png)

# ¿Cómo activar el modo desarrollador rápidamente?
La extensión para navegadores que todo usuario de Odoo debe tener se llama «Odoo debug» y está disponible, tanto para Google Chrome como para Mozilla Firefox. 
Aquí les dejó los enlaces de descarga:

[Odoo debug para Google Chrome](https://chrome.google.com/webstore/detail/odoo-debug/hmdmhilocobgohohpdpolmibjklfgkbi)

[Odoo debug para Mozilla Firefox](https://addons.mozilla.org/es/firefox/addon/odoo-debug)

La extensión es realmente fácil de usar. Al momento de instalarla, aparecerá el emoji del «mono» con los ojos tapados, indicándonos que no estamos en modo desarrollador. Si hacemos clic sobre el rostro del «mono», el emoji cambiará y aparecerá con la cara descubierta, reflejando que estamos en modo desarrollador y haciendo visible todas las opciones que Odoo muestra en este aspecto.
El modo desarrollador con los «assets» activados, también se puede activar con esta extensión, haciendo doble clic sobre el emoji, lo cual mostrará el rostro de un gorila.

# ¿Cómo instalar Odoo?
Hay varias formas de instalar Odoo, te dejo la referncia en su pág oficial 

[Aquí](https://www.odoo.com/documentation/13.0/administration/install/install.html#windows)

Pero yo en esta guía voy hacer referencia a la instalación en Windows como desarrollador que proporciona una mayor flexibilidad: por ejemplo, permite ejecutar varias versiones de Odoo en el mismo sistema. Bueno para desarrollar módulos, puede usarse como base para la implementación de producción.

**Instalación de origen**
La "instalación" de la fuente se trata realmente de no instalar Odoo y, en su lugar, ejecutarlo directamente desde la fuente.

Finalmente, proporciona un mayor control sobre la configuración del sistema y permite mantener (y ejecutar) más fácilmente múltiples versiones de Odoo una al lado de la otra.
Más➕ info [aquí](https://www.odoo.com/documentation/13.0/administration/install/install.html#setup-install-source)

**Clona el repositorio de Odoo con Git**

Edición de la comunidad:
```
C:\> git clone https://github.com/odoo/odoo.git
```
Enterprise Edition:
```
C:\> git clone https://github.com/odoo/enterprise.git
```
# Oddo con Python
Odoo requiere Python 3.6 o posterior para ejecutarse.
Asegúrese de que la versión sea 3.6 o superior, ya que las versiones anteriores no son compatibles con Odoo.
```
C:\> python --version
```
Verifique también que pip esta instalado
```
C:\> pip --version
```

# postgresql
Odoo utiliza PostgreSQL como sistema de gestión de base de datos.
Descargue e instale PostgreSQL 
[Aquí](https://www.postgresql.org/download/windows/)
Nota : versión compatible: 10.0 y posteriore
Más ➕ Nota importante:
De forma predeterminada, el único usuario es **postgres** pero Odoo prohíbe conectarse como postgres, por lo que debe crear un **nuevo usuario** de PostgreSQL:

 1. Add PostgreSQL’s bin directory (by default: C:\Program Files\PostgreSQL\<version>\bin) to your PATH.
2. Create a postgres user with a password using the pg admin gui:
 - Abra **pgAdmin**.
 - Haga doble clic en el servidor para crear una conexión.
 - Seleccione **Objeto ‣ Crear ‣ Rol de inicio de sesión/grupo**.
 - Introduzca el nombre de usuario en el campo **Nombre de rol** (por ejemplo, ).odoo
 - Abra la ficha Definición e introduzca la contraseña (por ejemplo, ) y, a continuación, haga clic en **Guardar**.
 - Abra la pestaña **Privilegios** y cambie **¿Puede iniciar sesión?** a y **Crear base de datos?**.👌

# virtualenv 
Antes de instalar Odoo en tu PC 🖥 lo primero que debes hacer es crearte un entorno virtual.
```
pip install virtualenv
```
## ¿Cómo crear un entorno virtual con Python?.
Ya tengo mís 🗒 sobre eso:

[Entornos virtuales](https://github.com/javierma73/Entornos-virtuales/blob/main/Entornos-virtuales.md)

Pero puedes consultar la referencia oficial: 
[virtualenv](https://pypi.org/project/virtualenv)
---
# ¿Quíero probar Odoo Ya?
En estos links puedes probar Odoo para ir **familiarizándote** con sus aplicaciones, es una **Demo,** así que puedes tocarlo todo, sin miedo a romperlo.

[TRIAL](https://www.odoo.com/es_ES/trial)

Referencia en la página Oficial de Odoo:
[Odoo en Línes](https://www.odoo.com/documentation/13.0/administration/install/install.html#online)

# Comparación de ediciones de Odoo
Odoo es un sistema de gestión empresarial (ERP) y un conjunto de aplicaciones empresariales de código abierto que ha experimentado varias ediciones a lo largo de su desarrollo. Aquí tienes un resumen comparativo de las ediciones más destacadas de Odoo:

1. **Odoo Community (CE - Edición Comunidad)**:
   - **Licencia**: Código abierto bajo la licencia LGPLv3.
   - **Características**: Ofrece una amplia gama de aplicaciones, incluyendo gestión de ventas, compras, inventario, CRM y más.
   - **Comunidad**: Desarrollado principalmente por la comunidad de código abierto y no tiene soporte oficial de Odoo S.A.
   - **Personalización**: Totalmente personalizable para adaptarse a las necesidades específicas de la empresa.
   - **Actualizaciones**: Actualizaciones regulares, pero no siempre al mismo ritmo que la edición Enterprise.

2. **Odoo Enterprise (EE - Edición Empresarial)**:
   - **Licencia**: Propietario con una suscripción de pago anual por usuario.
   - **Características**: Incluye todas las características de la edición Community y agrega módulos adicionales como Recursos Humanos, Helpdesk, y Marketing Automation.
   - **Soporte**: Ofrecido por Odoo S.A. con asistencia técnica y actualizaciones garantizadas.
   - **Actualizaciones**: Actualizaciones regulares y prioridad en nuevas características y mejoras.

3. **Odoo Online**:
   - **Despliegue**: Ofrecido como un servicio en la nube por Odoo S.A.
   - **Acceso**: Los usuarios pueden acceder a Odoo desde cualquier lugar con conexión a internet.
   - **Facilidad de uso**: No es necesario preocuparse por la administración de servidores ni actualizaciones.
   - **Costo**: Se paga una tarifa mensual por usuario.

4. **Odoo SH (Sh-Edición)**:
   - **Despliegue**: Ofrecido como una solución en la nube empresarial de alto rendimiento.
   - **Características**: Proporciona un rendimiento superior y escalabilidad para empresas con necesidades de alto tráfico.
   - **Personalización**: Permite una personalización profunda y acceso a nivel de código.
   - **Costo**: Precios basados en el uso y el rendimiento.

En resumen, Odoo ofrece una edición comunitaria de código abierto con características básicas y una edición empresarial con características avanzadas, soporte y actualizaciones garantizadas. Además, Odoo Online y Odoo SH ofrecen opciones de implementación en la nube para facilitar el acceso y la administración. La elección entre estas ediciones dependerá de las necesidades y el presupuesto de la empresa.

# Resumen ediciones de Odoo
- **Odoo Community (Edición Comunidad)**: Una edición de código abierto que ofrece una variedad de aplicaciones empresariales básicas y es mantenida principalmente por la comunidad de desarrolladores de Odoo.

- **Odoo Enterprise (Edición Empresarial)**: Una edición de pago que amplía las capacidades de la Comunidad con módulos adicionales y ofrece soporte oficial de Odoo S.A.

- **Odoo Online**: Una opción de implementación en la nube que permite a las empresas utilizar Odoo sin preocuparse por la infraestructura de servidores.

- **Odoo SH**: Una solución en la nube empresarial de alto rendimiento con escalabilidad y opciones de personalización avanzadas.
  
  Referencia:
  [Odoo Editions](https://www.odoo.com/es_ES/page/editions)

  # Precios y Planes
  
 [Precios](https://www.odoo.com/es_ES/pricing-plan)

![Precios y Planes]( https://github.com/javierma73/Odoo/blob/main/Precios%20Mensual%20de%20Odoo.png)

# Configuración del Entorno de Desarrollo

Antes de comenzar, necesitarás un entorno de desarrollo con Odoo instalado. Puedes optar por una instalación local o utilizar Docker, que es una opción popular por su facilidad de configuración y aislamiento.

[Odoo imagen oficial](https://hub.docker.com/_/odoo)

# Requisitos
- **Python**: Odoo requiere Python, generalmente Python 3.

- **PostgreSQL**: Base de datos compatible con Odoo.

- **Dependencias** de Odoo: Instala todas las librerías requeridas que Odoo necesita para funcionar.

**Creación del Esqueleto del Módulo**

Un módulo de Odoo es simplemente un directorio con un conjunto de archivos estructurados de manera específica:

- **__init__.py**: Archivo para inicializar el módulo, donde importas los modelos y controladores.
  
- **__manifest__.py**: Contiene metadatos del módulo como nombre, descripción, dependencias, etc.
  
Directorios para Modelos, Vistas, Datos, y Controladores: Organiza el código y los datos del módulo.

# Su primer módulo

[Su primer módulo](https://www.odoo.com/documentation/15.0/es/administration/odoo_sh/getting_started/first_module.html#your-first-module)

    

  







 









