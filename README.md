# Jornada — instalación y actualizaciones

Aquí se publica el **programa compilado** de Jornada, el registro horario (fichajes) para
talleres. El código fuente no está en este repositorio.

## Instalar (Linux, Ubuntu/Debian)

1. Descarga el último `jornada-X.Y.Z-linux-x86_64.tar.gz` de
   [Releases](https://github.com/Jchavanel/jornadas-release/releases/latest).
2. Instala las librerías de Qt (una sola vez):

   ```bash
   sudo apt install libxcb-cursor0 libegl1 libxkbcommon-x11-0
   ```

3. Descomprime y ejecuta el instalador (no necesita `sudo` ni Python):

   ```bash
   tar xzf jornada-X.Y.Z-linux-x86_64.tar.gz
   cd jornada-X.Y.Z
   ./install.sh                 # en el equipo del terminal: ./install.sh --autoarranque
   ```

## Actualizaciones

Jornada consulta `latest.json` de la última release y avisa en la administración cuando
hay una versión nueva. El administrador la instala con un clic: se hace una copia de los
datos, se comprueba la huella SHA-256 del paquete y el programa se reinicia. Los datos
(`~/.local/share/jornada`) nunca se tocan.
