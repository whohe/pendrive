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

## 🚀 Automatiza tu ISO personalizada con GitHub Actions

En lugar de repetir pasos manuales una y otra vez, este proyecto te permite usar **GitHub Actions** para generar tu ISO automáticamente cada vez que haces un cambio. Esto significa:

- Menos errores humanos.
- Más consistencia en cada nueva versión.
- Un sistema reproducible y controlado por versiones.

---

## 🪄 ¡Hazlo tuyo!

Este repositorio está diseñado para ser **forkeado**. Puedes adaptarlo fácilmente a tus necesidades:

- Cambia los paquetes que se instalan.
- Agrega tus propios archivos de configuración en `files/etc`.
- Modifica el arranque, temas de GRUB o configuraciones del sistema.

Todo el proceso está controlado por el manifiesto YAML que puedes modificar a voluntad.

---

## ☁️ Publica sin llenar tu repositorio

Subir automáticamente la ISO generada a servicios como **MEGA** o similares te permite:

- Liberar espacio en tu repositorio.
- Evitar los límites de almacenamiento de GitHub Releases.
- Compartir fácilmente tu sistema con otros mediante un enlace.

Este enfoque facilita la distribución sin comprometer la limpieza del repositorio principal.
