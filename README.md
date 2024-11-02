# Extract Ports

**Extract Ports** es una herramienta en Python para extraer la IP y puertos abiertos desde archivos de salida `nmap` en formato `-oG`, generando un comando `nmap` para escaneo detallado y copiándolo al portapapeles.

## Requisitos

- **Python 3.x**
- **Colorama** (`pip install colorama`)
- `xclip` en Linux o `pbcopy` en macOS para copiar al portapapeles.

## Instalación

1. Ubica el script en `/usr/bin`:
   ```bash
   sudo mv extract_ports.py /usr/bin/extractPorts.py
   ```

2. Otorga permisos de ejecución:
   ```bash
   sudo chmod +x /usr/bin/extractPorts.py
   ```

3. Agrega un alias en `.zshrc` o `.bashrc` para facilitar su uso. Abre el archivo con un editor de texto, como `nano`:
   ```bash
   nano ~/.zshrc    # o nano ~/.bashrc
   ```

4. Añade esta línea al final del archivo:
   ```bash
   alias extractPorts='/usr/bin/extractPorts.py'
   ```

5. Guarda y cierra el archivo, luego recarga la configuración:
   ```bash
   source ~/.zshrc   # o source ~/.bashrc
   ```

## Uso

```bash
extractPorts <archivo>
```

**Ejemplo**:
```bash
extractPorts scan_output.txt
```

Esto mostrará la IP y puertos abiertos, además de generar y copiar el comando de escaneo detallado a tu portapapeles.

