# Extract Ports

**Extract Ports** es una herramienta en Python que permite extraer la dirección IP y puertos abiertos desde archivos de salida `nmap` en formato `-oG`. También genera un comando `nmap` para un escaneo detallado y lo copia automáticamente al portapapeles.

## Requisitos

- **Python**
- **Colorama**: Instalación mediante `pip`
  ```bash
  pip install colorama
  ```
- **xclip**: Instalación para copiar al portapapeles:
  ```bash
  sudo apt install xclip
  ```

## Instalación

1. Mueve el script a `/usr/bin` para facilitar su acceso global:
   ```bash
   sudo mv extractPorts.py /usr/bin/extractPorts.py
   ```

2. Asigna permisos de ejecución al script:
   ```bash
   sudo chmod +x /usr/bin/extractPorts.py
   ```

3. Crea un alias para facilitar su uso desde cualquier terminal. Abre tu archivo de configuración (`.zshrc` o `.bashrc`):
   ```bash
   nano ~/.zshrc   # O usa nano ~/.bashrc según tu shell
   ```

4. Agrega el siguiente alias al final del archivo:
   ```bash
   alias extractPorts='/usr/bin/extractPorts.py'
   ```

5. Guarda y cierra el archivo, luego recarga la configuración del shell:
   ```bash
   source ~/.zshrc   # O usa source ~/.bashrc si corresponde
   ```

## Uso

Ejecuta el comando `extractPorts` seguido del archivo de salida de `nmap`:

```bash
extractPorts <archivo>
```

**Ejemplo**:
```bash
extractPorts allPorts
```
![image](https://github.com/user-attachments/assets/4f845a8c-20a4-4637-9b8e-ae058d22d95d)

Esto mostrará la dirección IP y los puertos abiertos detectados, además de copiar el comando `nmap` de escaneo detallado al portapapeles para que puedas pegarlo directamente en la terminal.





