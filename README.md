# Configuración del entorno para el proyecto Notebook-MachineLearning

Para gestionar versiones de Python en Windows usaremos [pyenv-win](https://github.com/pyenv-win/pyenv-win).

Este README explica cómo preparar el entorno de desarrollo utilizando **pyenv-win** para manejar versiones de Python, instalar Python 3.11.9 y crear un entorno virtual.

---

## Requisitos previos

- Git instalado en tu sistema.
- Acceso a la terminal (PowerShell, CMD o Git Bash en Windows).

---

# Paso 1: Instalar pyenv-win

Para la instalación de pyenv-win mediante comandos git en este proyecto es recomendable seguir el [tutorial de instalación.](https://github.com/pyenv-win/pyenv-win/blob/master/docs/installation.md#git-commands), sin embargo, dentro de ese mismo repositorio encontrarás otras formas de instalación para que realices la que mejor te parezca.


Luego de agregar las variables de entorno en tu perfil para que **pyenv** esté disponible en la terminal, es recomendable reiniciar la terminar y ejecutar:

```bash
pyenv --version
```

# Paso 2: Instalar Python 3.11.9

Con pyenv instalado, instala la versión de Python requerida para el proyecto:

```bash
    pyenv install 3.11.9
```

Configura la versión local de Python para este proyecto:

```bash
pyenv local 3.11.9
```

Verifica que la versión está activa:

```bash
pyenv versions
```
Deberías ver 3.11.9 marcada con un asterisco (*) indicando que está activa.

# Paso 3: Crear y activar entorno virtual

Desde la carpeta raíz del proyecto ejecuta:

```bash
python -m venv tf-env
```
*Puedes reemplazar 'tf-env' por el nombre que desees ponerle a tu entorno virtual.*

En caso de no servir puede usar la python.exe del root (cambiar "tu-usuario" por el nombre de tu usuario) ejecuta este comando:

```bash
 C:\Users\tu-usuario\.pyenv\pyenv-win\versions\3.11.9\python.exe -m venv tf-env
```

Activa el entorno virtual:

En PowerShell:

```bash
.\tf-env\Scripts\Activate.ps1
```

En CMD:

```bash
.\tf-env\Scripts\activate.bat
```

Verifica la versión de Python dentro del entorno:

```bash
python --version
```
# Paso 4: Instalar dependencias

Instalamos dependencias con el comando pip:

```bash
 pip install numpy pandas matplotlib seaborn pillow opencv-python scikit-learn tensorflow
```

# Paso 5: Cambiar Kernel de Jupyter

Simplemente vamos a Visual Studio Code y al abrir tu archivo de Jupyter, en la parte superior derecha donde diga "_Seleccionar kernel_", vas a dar click, lo que desplegará un menú para que elijas los entornos de python a usar.

![Paso 1. Seleccionar el kernel de python.](https://drive.google.com/uc?export=view&id=1nNYSDzYJVX-VsaugYfLb-EsZsQ68GW1e)

Escoger el entorno de python (pyenv), en su versión 3.11.9 (o la que hayas elegido usar). 

![Paso 2. Escoger la version a usar.](https://drive.google.com/uc?export=view&id=16qRTJrs28MvLwanNWlEhzPLxxB7PpyHm)

Por último, verifica que se haya seleccionado correctamente, arriba a la derecha donde decía "_Seleccionar kernel_", ahora debería aparecer la versión del entorno de python que hayas escogido.

![Paso Final. Verificar selección de entorno.](https://drive.google.com/uc?export=view&id=1FRaIS-7VV9bwY3Qhdrs7F-0odUlzQqTd)