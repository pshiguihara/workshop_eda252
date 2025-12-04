# Workshop de Algoritmos y Estructuras de Datos


# Sistema de Gestión de Paquetes y Entornos (Conda)

## Instalar Conda
[Miniforge](https://github.com/conda-forge/miniforge)

## Instalar PyCharm
[PyCharm](https://www.jetbrains.com/es-es/pycharm/download/)


## ¿Qué es Conda?
Conda es un sistema *open‑source* para:
- **Gestión de paquetes**: instalar, actualizar y administrar dependencias.
- **Gestión de entornos**: crear, clonar, activar y administrar entornos con versiones específicas de Python u otros lenguajes.

Compatible con Windows, macOS y Linux.

---

## 1. Conda: Dos sistemas en uno

### Como gestor de paquetes:
- Instalar, ejecutar y actualizar paquetes.
- Resolver dependencias desde canales.

### Como gestor de entornos:
- Crear, cargar y cambiar entre entornos.
- Usar versiones diferentes de Python aisladas entre sí.

---

## 2. Paquetes Conda
Un **paquete conda** es un archivo `.tar.bz2` o `.conda` que contiene:
- Librerías del sistema.
- Módulos de Python u otros lenguajes.
- Ejecutables.
- Metadatos de instalación.

---

## 3. Canales Conda
Un **canal** contiene colecciones de paquetes.  
Conda usa el índice del canal para resolver versiones y dependencias.

Ejemplos:
- `conda-forge`
- `defaults`

---

## 4. Entornos Conda

### Crear entornos
```bash
conda create --name <ENTORNO>
conda create -n <ENTORNO>
```

### Crear entorno con versión específica de Python
```bash
conda create -n <ENTORNO> python=3.10
```

### Crear entorno desde archivo YML
```bash
conda env create -f <ARCHIVO>.yml
```

### Activar / desactivar
```bash
conda activate <ENTORNO>
conda deactivate
```

### Listar entornos
```bash
conda env list
```

### Exportar entorno
Con dependencias exactas:
```bash
conda env export > entorno.yml
```

Basado en histórico:
```bash
conda env export --from-history > entorno.yml
```

### Eliminar entorno
```bash
conda env remove -n <ENTORNO>
conda remove -n <ENTORNO> --all
```

---

## 5. Gestión de Paquetes

### Buscar paquete
```bash
conda search <PAQUETE>
```

### Instalar paquete
```bash
conda install <PAQUETE>
```

### Instalar desde un canal
```bash
conda install -c <CANAL> <PAQUETE>
conda install <CANAL>::<PAQUETE>
```

### Instalar versión específica
```bash
conda install <PAQUETE>=3.1.4
```

### Listar paquetes del entorno activo
```bash
conda list
conda list --show-channel-urls
```

---

## 6. Instalación de Conda
Se puede instalar a través de:

- **Miniforge**: https://github.com/conda-forge/miniforge  
- **Miniconda**: https://docs.conda.io/projects/miniconda/en/latest/  
- **Anaconda**: https://www.anaconda.com/  

**Mamba** (acelerado en C++):  
https://github.com/mamba-org/mamba

---

## 7. Comandos de configuración

Inicializar conda en terminal:
```bash
conda init
```

Ver versión:
```bash
conda --version
```

Agregar canal:
```bash
conda config --add channels <CANAL>
```

Ver canales:
```bash
conda config --show channels
```

---

## 8. Limpieza de paquetes y caché

Eliminar caché:
```bash
conda clean
```

Eliminar paquetes no usados:
```bash
conda clean -p
conda clean --packages
```

Eliminar tarballs:
```bash
conda clean -t
```

Eliminar todo:
```bash
conda clean -a
```

Combinación (tarballs + paquetes no usados):
```bash
conda clean -tp
```

---

## 9. Conclusiones
- La gestión de paquetes permite obtener módulos desde la nube y reproducir entornos de forma ágil para análisis de datos.
- La gestión de entornos asegura compatibilidad entre miembros de un equipo, facilitando reproducibilidad y transferencia.

---

