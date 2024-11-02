

# Extract Ports

**Extract Ports** es una herramienta en Python para extraer la IP y puertos abiertos desde archivos de salida `nmap` en formato `-oG`, generando un comando `nmap` para escaneo detallado y copiándolo al portapapeles.

## Requisitos

- **Python 3.x**
- **Colorama** (`pip install colorama`)
- `xclip` en Linux o `pbcopy` en macOS para copiar al portapapeles.

## Uso

```bash
python3 extractPorts.py <archivo>
```

**Ejemplo**:
```bash
python3 extractPorts.py allPorts
```

Esto mostrará la IP y puertos abiertos, además de generar y copiar el comando de escaneo detallado a tu portapapeles.
