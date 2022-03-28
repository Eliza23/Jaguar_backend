# Proyecto Jaguar_backend
## Creación de un proyecto con Django. 
1. Instalar Python 3.9.11 <br>
		https://www.python.org/  <br>
2. Crear el entorno virtual (en la carpeta dev, en este caso) <br>
		python -m venv dev  <br> 
3. Activar el entorno virtual   <br> 
   		cd dev  <br>
   		.\Scripts\activate  <br>
4. Instalar django. <br>
		python -m pip install Django <br> 
5. Crear el proyecto jaguar-backend.   <br>
		django-admin startproject jaguar_backend  <br>

## Instalar el Proyecto.
1. Instalar Python 3.9.11 </br>
https://www.python.org/   </br>
2. Descargar el proyecto desde el repositorio de github.   </br>
3. git clone https://github.com/Eliza23/Jaguar_backend.git 

## Crear lista de dependencia
1. Instalar dependencias. <br>
	pip install nombre_paquete. 
2. Ver dependencias instalados. </br>
	pip freeze 
3. Crear elarchivo con la lista de dependencias. <br>
	pip freeze > requeriments.txt 
4. Instalar la lista de dependencias del proyecto. <br>
	pip install -r requeriments.txt 

## Empaquetar proyecto Django
1. Crear el proyecto con DJango (jaguar-backend) 
2. Copiar el proyecto en una carpeta (jaguar_backend_dist)
3. Dentro de la nueva carpeta, crear los archivos LICENCE, pyproyect.toml, README.md y setup.py 
4. Copiar contenido en cada archivo. <br>
4.1. En el archivo pyproyect.toml <br>
		[build-system] </br>
      requires = ["setuptools>=42"] </br>
      build-backend = "setuptools.build_meta" </br>
4.2. En el archivo setup.py  </br>
      import setuptools </br>
      with open("README.md", "r", encoding="utf-8") as fh: </br>
         long_description = fh.read() </br>
         setuptools.setup( </br>
            name="example-package-YOUR-USERNAME-HERE", </br>
            version="0.0.1", </br>
            author="Example Author", </br>
            author_email="author@example.com", </br>
            description="A small example package", </br>
            long_description=long_description, </br>
            long_description_content_type="text/markdown", </br>
            url="https://github.com/pypa/sampleproject", </br>
            project_urls={ </br>
               "Bug Tracker": "https://github.com/pypa/sampleproject/issues", </br>
            }, </br>
            classifiers=[ </br>
               "Programming Language :: Python :: 3", </br>
               "License :: OSI Approved :: MIT License", </br>
               "Operating System :: OS Independent", </br>
            ], </br>
            package_dir={"": "jaguar_backend"}, </br>
            packages=setuptools.find_packages(where="jaguar_backend"), </br>
            python_requires=">=3.9", </br>
         )  </p>
5. Ejecutar los comandos para generar los paquetes de distribucion: </br>
	<strong> py -m pip install --upgrade build </strong> </br>
	<strong> py -m build </strong></p>
6. Esto generara una nueva carpeta llamada dist que tiene 2 archivos: </br>
	      El tar.gzq que es un archivo fuente y el .whl es una distribución construida. </br>
            dist/</br>
               example-package-YOUR-USERNAME-HERE-0.0.1-py3-none-any.whl</br>
               example-package-YOUR-USERNAME-HERE-0.0.1.tar.gz
7. Instalar el proyecto </br> 
7.1. Descompirmir el archivo .tar.gz </br> 
7.2. Ejecutar el comando python setup.py install


