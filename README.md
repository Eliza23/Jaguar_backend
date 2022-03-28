# Proyecto Jaguar_backend
## Creación de un proyecto con Django. 
1. Instalar Python 3.9.11 <br>
[https://www.python.org/](link)
		  <br>
2. Crear el entorno virtual (en la carpeta dev, en este caso) <br>
```html 
	python -m venv dev 
```
3. Activar el entorno virtual   <br> 
```html   		
	cd dev 
	.\Scripts\activate 
```
4. Instalar django. <br>
```html 
	python -m pip install Django
```
5. Crear el proyecto jaguar-backend.   <br>
```html 
	django-admin startproject jaguar_backend 
```
## Instalar el Proyecto.
1. Instalar Python 3.9.11 </br>
https://www.python.org/   </br>
2. Descargar el proyecto desde el repositorio de github.   </br>
3. git clone https://github.com/Eliza23/Jaguar_backend.git 

## Crear lista de dependencia
1. Instalar dependencias. <br>
```html 
	pip install nombre_paquete. 
```
2. Ver dependencias instalados. </br>
```html 
	pip freeze 
```
3. Crear elarchivo con la lista de dependencias. <br>
```html 
	pip freeze > requeriments.txt 
```
4. Instalar la lista de dependencias del proyecto. <br>
```html 
	pip install -r requeriments.txt 
```
## Empaquetar proyecto Django
1. Crear el proyecto con DJango (jaguar-backend) 
2. Copiar el proyecto en una carpeta (jaguar_backend_dist)
3. Dentro de la nueva carpeta, crear los archivos LICENCE, pyproyect.toml, README.md y setup.py 
4. Copiar contenido en cada archivo. <br>
4.1. En el archivo pyproyect.toml <br>
```html 
	[build-system] 
      	requires = ["setuptools>=42"] 
      	build-backend = "setuptools.build_meta"
```
4.2. En el archivo setup.py  </br>
```html 
      import setuptools 

      with open("README.md", "r", encoding="utf-8") as fh:
         long_description = fh.read() 
         setuptools.setup(
            name="example-package-YOUR-USERNAME-HERE", 
            version="0.0.1", 
            author="Example Author", 
            author_email="author@example.com",
            description="A small example package", 
            long_description=long_description, 
            long_description_content_type="text/markdown", 
            url="https://github.com/pypa/sampleproject", 
            project_urls={ 
               "Bug Tracker": "https://github.com/pypa/sampleproject/issues",
            }, 
            classifiers=[ 
               "Programming Language :: Python :: 3",
               "License :: OSI Approved :: MIT License", 
               "Operating System :: OS Independent", 
            ],
            package_dir={"": "jaguar_backend"}, 
            packages=setuptools.find_packages(where="jaguar_backend"), 
            python_requires=">=3.9",
         )  
```

5. Ejecutar los comandos para generar los paquetes de distribucion: </br>
```html 
	py -m pip install --upgrade build
	py -m build 
```
6. Esto generara una nueva carpeta llamada dist que tiene 2 archivos: </br>
	* El tar.gzq que es un archivo fuente y el .whl es una distribución construida. </br>
	* dist/ <br>
   		example-package-YOUR-USERNAME-HERE-0.0.1-py3-none-any.whl</br>
    		example-package-YOUR-USERNAME-HERE-0.0.1.tar.gz <br>
7. Instalar el proyecto <br>
7.1. Descompirmir el archivo .tar.gz <br>
7.2. Ejecutar el comando  <br>
```html 
	python setup.py install
```

