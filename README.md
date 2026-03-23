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
> **1. Login y Menú Principal**
<img width="370" height="399" alt="image" src="https://github.com/user-attachments/assets/3bc178ea-d14f-4a21-9209-ae6518a05171" />

<img width="370" height="399" alt="image" src="https://github.com/user-attachments/assets/1772c05e-d95c-451b-a902-8a14e02f8226" />


> **2. Bandeja de Despachos y Detalles**
<img width="1010" height="892" alt="image" src="https://github.com/user-attachments/assets/6fcc7d34-6b79-4e7a-829d-fc5f772acb4d" />

<img width="1115" height="715" alt="image" src="https://github.com/user-attachments/assets/b525ef7c-1185-4934-9949-a9897b8b3ac8" />



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
