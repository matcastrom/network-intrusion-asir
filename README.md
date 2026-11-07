Trabajo de Pandas -- 2.º ASIR
El informe completo está en index.qmd.

1. Preparar los datos
Descarga el conjunto de datos desde:

https://www.kaggle.com/datasets/sampadab17/network-intrusion-detection

Copia los dos CSV dentro de la carpeta data/ y utiliza estos nombres:
- Train_data.csv
- Test_data.csv
La estructura debe ser:
network_intrusion_asir/
├── index.qmd
├── README.md
├── requirements.txt
├── .gitignore
└── data/
    ├── Train_data.csv
    └── Test_data.csv
  
2. Instalar las librerías
Necesitas tener Python y Quarto instalados. Con la terminal abierta en
esta carpeta, crea y activa un entorno virtual.

Windows (PowerShell):
py -m venv .venv
.\.venv\Scripts\Activate.ps1
Si PowerShell bloquea la activación, ejecuta antes:
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
Linux:
python3 -m venv .venv
source .venv/bin/activate
Con el entorno virtual activado, instala las librerías:
python -m pip install -r requirements.txt
En Linux, si python no está disponible, utiliza python3.

Quarto se instala por separado desde
https://quarto.org/docs/get-started/. Comprueba que está disponible con
quarto --version.

3. Generar el informe
Ejecuta desde esta carpeta:
quarto render index.qmd
Quarto generará index.html en esta misma carpeta. Abre ese archivo con
el navegador para revisar el informe.

4. Publicar con GitHub Pages
1. Crea un repositorio público en GitHub.
2. Sube index.qmd, index.html, README.md, .gitignore y la
   carpeta data/ (si la licencia del conjunto de datos permite
   compartir los CSV).
3. En GitHub abre Settings > Pages.
4. En Build and deployment, selecciona Deploy from a branch.
5. Selecciona la rama main y la carpeta /(root).
6. Guarda los cambios. GitHub Pages publicará el index.html que
   generó Quarto.
Cada vez que modifiques el informe, vuelve a ejecutar
quarto render index.qmd y sube el nuevo index.html junto con los
cambios.
