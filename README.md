# ManteniPro releases

Distribución pública de ManteniPro para Windows 11 x64. El código fuente permanece en repositorios privados; la instalación no requiere clonar repositorios ni iniciar sesión en npm, GitHub o GHCR.

## Instalar

1. Instalá Node.js 24 y Docker Desktop. Iniciá Docker en modo contenedores Linux.
2. Abrí PowerShell como Administrador e instalá la CLI:

   ```powershell
   npm install -g @mantenipro/cli@latest
   ```

3. Instalá ManteniPro:

   ```powershell
   mantenipro install
   ```

4. Definí la contraseña del administrador y abrí la URL HTTPS indicada. El usuario es `admin`.

El comando usa el canal **stable**, el puerto **8443** y `C:\ManteniPro`. `mantenipro install --port 8443` también es válido. No hace falta `--channel candidate` ni `--channel-url`.

## Actualizar

Actualizá primero una CLI antigua con el mismo comando npm de arriba. Para actualizar una instalación existente:

```powershell
mantenipro update
```

Consulta stable, pide confirmación y realiza un backup verificado antes de aplicar cambios. `mantenipro update --check` solamente consulta la versión disponible.

## Desinstalar

```powershell
mantenipro uninstall
```

Pide confirmación y conserva datos, backups, certificados y configuración por defecto. No borra datos de la planta sin las opciones y la confirmación adicional de eliminación. Ver `mantenipro uninstall --help`.

## Versiones e integridad

Release stable: **1.0.7**. CLI mínima: **0.1.7**.

La [última release estable](https://github.com/NicolasUrdiales/mantenipro-releases/releases/latest) contiene el bundle, manifiesto, firmas Ed25519, hashes e índice del canal. La CLI verifica estos artefactos antes de modificar Docker. Las imágenes también están publicadas para descarga anónima y fijadas por digest.

Las notas de cada release detallan cambios, pruebas realizadas y límites de la validación. Las releases candidate no desplazan el canal stable.
