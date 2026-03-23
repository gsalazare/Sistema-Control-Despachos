# Sistema de Control de Despachos 📦

Un sistema corporativo desarrollado en Microsoft Access y VBA para la gestión de requerimientos, transferencias de almacén y despachos. Diseñado para optimizar el flujo de trabajo en áreas de logística e inventarios.

## 🚀 Características Principales

* **Arquitectura Dividida (Split Database):** Separación de la capa de datos (Back-end) y la capa de interfaz (Front-end) para permitir trabajo en red multiusuario sin corrupción de datos.
* **Sistema de Login y Roles:** Control de acceso encriptado mediante variables temporales (`TempVars`). Rutas de navegación dinámicas dependiendo del rol (Administrador vs. Operador).
* **Trazabilidad y Auditoría ("Caja Negra"):** Registro automático y silencioso mediante inyección SQL de cada cambio de estado, capturando el usuario exacto, el requerimiento y la fecha/hora de la transacción.
* **Interfaz Optimizada (UX/UI):** Formularios limpios, botones de acción controlados por macros VBA, y refresco automático de bandejas en tiempo real.

## 🛠️ Tecnologías Utilizadas
* **Microsoft Access** (Motor de base de datos relacional)
* **VBA (Visual Basic for Applications)** (Lógica de negocio y automatizaciones)
* **SQL** (Consultas y manipulación de datos)

## 📖 Instrucciones de Prueba

Para probar este sistema de forma local:
1. Descarga ambos archivos (`.accdb`) en una misma carpeta.
2. Abre el archivo **Front-end**.
3. Ve a la pestaña *Datos externos* > *Administrador de tablas vinculadas* y vuelve a vincular las tablas apuntando al archivo **Back-end** descargado.
4. Usa las siguientes credenciales de demostración:
   * **Rol Admin:** Usuario: `admin_demo` | Clave: `123`
   * **Rol Operador:** Usuario: `operador_demo` | Clave: `123`
