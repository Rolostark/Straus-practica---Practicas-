---

kanban-plugin: board

---

## Fase 1: Preparación de Hardware y RAID

- [ ] **Montaje físico:** Desembalar y ubicar el servidor HPE ProLiant ML30 Gen11. Instalar físicamente los 2 discos duros Seagate BarraCuda de 2TB en las bahías del servidor.
	[[01 montaje fisico]]
- [ ] **Configuración de almacenamiento (RAID):** Acceder a la controladora de discos de HPE para crear los volúmenes lógicos.
	
	- Configurar un RAID 1 (espejo) con los dos discos SSD de 480GB para el sistema operativo.
	    
	- Configurar los dos discos Seagate de 2TB para la unidad de documentos en red y copias de seguridad (recomendable también en RAID 1 para tolerancia a fallos).


## Fase 2: Instalación del Sistema Operativo y Licenciamiento

- [ ] **Despliegue del SO:** Instalar la licencia de Microsoft Windows Server 2025 Standard ROK en el volumen SSD.
- [ ] **Actualizaciones:** Instalar los controladores (drivers) específicos de HPE y descargar las últimas actualizaciones de seguridad de Windows.
- [ ] **Licenciamiento de usuarios:** Configurar e instalar las licencias CAL para habilitar el acceso legal de hasta 10 usuarios.


## Fase 3: Configuración de Red y Directorio Activo (Active Directory)

- [ ] **Red:** Asignar una dirección IP estática al servidor dentro de la red de CAMINERO & PRADO ASOCIADOS SL.
- [ ] **Roles del servidor:** Instalar los roles de Servicios de Dominio de Active Directory (AD DS), DNS y servidor de archivos.
- [ ] **Creación de usuarios:** Dar de alta a los usuarios (hasta 10) en el dominio para centralizar la gestión de contraseñas y permisos.


## Fase 4: Estructura de Almacenamiento y Carpetas Compartidas

- [ ] **Volumen de datos:** Dar formato a la unidad de discos Seagate de 2TB.
- [ ] **Árbol de directorios:** Crear la estructura de carpetas de la empresa (Gerencia, Contabilidad, Recursos Humanos, etc.).
- [ ] **Permisos:** Aplicar los permisos de seguridad (NTFS y permisos de red) para que cada usuario solo vea o edite lo que le corresponde.


## Fase 5: Traspaso de Datos y Copias de Seguridad

- [ ] **Migración:** Extraer y transferir toda la información desde el servidor antiguo o los ordenadores individuales de los usuarios hacia la nueva unidad de documentos en red.
- [ ] **Automatización de Backups:** Configurar una herramienta de copia de seguridad (por ejemplo, Windows Server Backup) para realizar respaldos diarios automatizados utilizando el espacio designado en los discos de 2TB.


## Fase 6: Puesta en Marcha y Pruebas

- [ ] **Unión de equipos:** Unir los ordenadores de los trabajadores al nuevo dominio.
- [ ] **Mapeo de unidades:** Configurar un script o políticas de grupo (GPO) para que la unidad de red compartida aparezca automáticamente en los ordenadores de los 10 usuarios.
- [ ] **Verificación:** Comprobar que los usuarios acceden a los datos correctamente, que el software de gestión funciona y que las copias de seguridad se ejecutan sin errores.




%% kanban:settings
```
{"kanban-plugin":"board","list-collapse":[false,false,false,false,false,false]}
```
%%