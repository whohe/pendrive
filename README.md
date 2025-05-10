## 📦 pendrive.iso Workflow  
Este proyecto automatiza la creación de una imagen ISO personalizada, preparada para ser instalada en una memoria USB (pendrive) con características específicas como persistencia de datos y cifrado. El workflow está definido en `.github/workflows/pendrive.yml`.

---

## 🧠 ¿Por qué crear tu propia ISO booteable en un pendrive?

Tener un sistema Linux hecho a tu medida y listo para llevar a cualquier parte no es solo una curiosidad técnica: es una herramienta poderosa. Un pendrive personalizado te permite:

- ✅ Acceder a tu entorno de trabajo desde cualquier equipo.
- 🔐 Proteger tus datos con cifrado completo.
- ⚙️ Incluir tus propias herramientas, scripts y configuraciones.
- 💾 Disfrutar de persistencia para guardar cambios entre reinicios.
- 🔄 Recuperar sistemas o trabajar en modo *rescate* con tus propias herramientas.

---

## 📦 Descripción
Pendrive es una distribución personalizada basada en Debian, diseñada para proporcionar un entorno portátil, seguro y optimizado para tareas específicas como recuperación del sistema o uso en entornos controlados. Incluye configuraciones predefinidas, herramientas seleccionadas y personalización visual (pantalla de inicio y fondo de escritorio).

---
## 🚀 Características

- Basado en Debian con entorno de escritorio personalizado.
- Persistencia de datos y cifrado de almacenamiento.
- Herramientas preinstaladas para recuperación y diagnóstico.
- Personalización visual con temas y fondos específicos.
---
## 🛠️ Requisitos del Sistema

- Memoria USB de al menos 8 GB.
- PC con capacidad de arranque desde USB.
- Procesador compatible con arquitectura x86_64.
---
## 🚀 Automatiza tu ISO personalizada con GitHub Actions

En lugar de repetir pasos manuales una y otra vez, este proyecto te permite usar **GitHub Actions** para generar tu ISO automáticamente cada vez que haces un cambio. Esto significa:

- Menos errores humanos.
- Más consistencia en cada nueva versión.
- Un sistema reproducible y controlado por versiones.

---
## 🔐 Credenciales Predeterminadas

- **Usuario:** WHO
- **Contraseña:** secret

> ⚠️ Por razones de seguridad, se recomienda cambiar estas credenciales después de la instalación inicial.

---
## 📥 Instalación

1. Descarga la imagen ISO desde la sección de [Releases](https://github.com/whohe/pendrive/releases).
2. Verifica la integridad de la ISO utilizando el archivo `pendrive.iso.sha256`.
3. Utiliza una herramienta como `dd` o `Etcher` para grabar la ISO en la memoria USB.
4. Inserta la memoria USB en el equipo y arranca desde ella.
---
## 🧪 Uso

- Inicia sesión con las credenciales predeterminadas.
- Accede a las herramientas preinstaladas desde el menú principal.
- Guarda tus archivos en el almacenamiento persistente.
---
## 🪄 ¡Hazlo tuyo!

Este repositorio está diseñado para ser **forkeado**. Puedes adaptarlo fácilmente a tus necesidades:

- Cambia los paquetes que se instalan.
- Agrega tus propios archivos de configuración en `files/etc`.
- Modifica el arranque, temas de GRUB o configuraciones del sistema.

Todo el proceso está controlado por el manifiesto YAML que puedes modificar a voluntad.

---
## 🧰 Personalización

- Modifica el archivo `packages.txt` para agregar o eliminar paquetes.
- Personaliza la configuración del sistema en el directorio `scratch/`.
- Actualiza el fondo de escritorio reemplazando `wallpaper.jpg`.
---
### 🔄 Personalización Segura de la Contraseña

Para mejorar la seguridad del sistema, se recomienda cambiar la contraseña predeterminada **antes de compilar la imagen ISO**. La forma más sencilla es haciendo un **fork del repositorio** y modificando el manifiesto de GitHub Actions.

#### 🔧 Método Básico

1. Haz un **fork** de este repositorio.
2. Ve al archivo `.github/workflows/pendrive.yml`.
3. Busca la sección donde se define la variable `PASSWORD`.
4. Sustituye el valor `"secret"` por una contraseña personalizada:

```yaml
env:
  USERNAME: WHO
  PASSWORD: tu_contraseña_segura_aquí
```
---
⚠️ **Advertencia:** Si tu repositorio es público, no pongas contraseñas directamente en el manifiesto.

---

#### 🛡️ Método Recomendado: Usar GitHub Secrets

Para mantener la contraseña segura incluso en repositorios públicos:

1. Abre tu fork en GitHub.
2. Ve a **Settings > Secrets and variables > Actions**.
3. Crea un nuevo secreto llamado `ISO_PASSWORD`.
4. Edita el archivo `.github/workflows/pendrive.yml` y usa el secreto así:

```yaml
env:
  USERNAME: WHO
  PASSWORD: ${{ secrets.ISO_PASSWORD }}
```
---
## ☁️ Publica sin llenar tu repositorio

Subir automáticamente la ISO generada a servicios como **MEGA** o similares te permite:

- Liberar espacio en tu repositorio.
- Evitar los límites de almacenamiento de GitHub Releases.
- Compartir fácilmente tu sistema con otros mediante un enlace.

Este enfoque facilita la distribución sin comprometer la limpieza del repositorio principal.

---
## 🤝 Contribuciones

¡Las contribuciones son bienvenidas! Por favor, abre un issue o envía un pull request para sugerir mejoras o reportar problemas.

---
## 📄 Licencia

Este proyecto está licenciado bajo la Licencia GPL-3.0. Consulta el archivo [LICENSE](LICENSE) para más información.

