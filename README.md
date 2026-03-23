# 📦 Sistema de Control de Despachos (WMS-Lite)

![Access](https://img.shields.io/badge/Microsoft_Access-A4373A?style=for-the-badge&logo=microsoft-access&logoColor=white)
![VBA](https://img.shields.io/badge/VBA-000080?style=for-the-badge&logo=visual-basic&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)

Un sistema de gestión corporativo diseñado para optimizar el flujo de requerimientos, transferencias entre almacenes y control de despachos. Construido para eliminar cuellos de botella operativos, asegurar la trazabilidad de los movimientos y blindar la información mediante arquitectura dividida.

## 🎯 Visión del Proyecto
Este desarrollo nace de la necesidad operativa de tener un control estricto sobre las salidas de almacén. Reemplaza el seguimiento manual o en hojas de cálculo aisladas por un entorno multiusuario seguro, reduciendo errores de digitación y tiempos de respuesta en la cadena de suministro.

## 🚀 Funcionalidades Core

* **Arquitectura Split-Database:** Separación técnica de Datos (Back-end) e Interfaz (Front-end) alojada en red, previniendo la corrupción de archivos bajo uso simultáneo.
* **Seguridad y Control de Roles:** Autenticación de usuarios con gestión de sesiones en memoria (`TempVars`). Navegación dinámica inteligente que adapta la interfaz si el usuario es Administrador o perfil Operativo.
* **Motor de Auditoría Oculto ("Caja Negra"):** Trazabilidad 100% automatizada. Cada cambio de estado inyecta silenciosamente un registro SQL con el autor, ID de transacción y Timestamp exacto.
* **UX Logística:** Flujos de trabajo optimizados para rapidez. Bandejas de auto-refresco y menús modales que mantienen al operario enfocado en la tarea de despacho.

## 💻 Interfaz del Sistema

*(Nota: Aquí puedes arrastrar y soltar capturas de pantalla de tu menú, login y bandeja)*
> **1. Menú Principal y Login**
> [Espacio para Imagen]
> 
> **2. Bandeja de Despachos y Detalles**
> [Espacio para Imagen]

## 🛣️ Roadmap (Próximas Mejoras)
El sistema está en mejora continua. Las siguientes integraciones están en fase de desarrollo:
- [ ] Conexión ODBC de solo lectura con **SAP Business One** para auto-completado de maestros de artículos.
- [ ] Alertas automatizadas por correo electrónico vía integración con MS Outlook.
- [ ] Conexión del Back-end a **Power BI** para tableros de rendimiento de almacén.

## ⚙️ Despliegue Local (Demo)

Para auditar la estructura y probar el sistema localmente:
1. Clonar o descargar el repositorio.
2. Abrir el archivo `_FrontEnd.accdb` (asegurarse de que ambos archivos estén en la misma ruta).
3. Utilizar el Administrador de Tablas Vinculadas de Access para reconectar con el `_BackEnd.accdb`.
4. **Credenciales de prueba:**
   * Supervisor: `admin_demo` | Clave: `123`
   * Almacén: `operador_demo` | Clave: `123`
