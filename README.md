# Proyecto Jaguar_backend
   Creación de un proyecto con Django. 
      Instalar Python 3.9.11 
         https://www.python.org/ 
      Crear el entorno virtual (en la carpeta dev, en este caso) 
         python -m venv dev   
      Activar el entorno virtual   
         cd dev  
         .\Scripts\activate  
      Instalar django. 
         python -m pip install Django  
      Crear el proyecto jaguar-backend.   
         django-admin startproject jaguar_backend  


   <h3>  Instalar el Proyecto.</h3>
      <p> <strong> 1. </strong>Instalar Python 3.9.11 </br>
      <strong> https://www.python.org/ </strong> </p>
      <p> <strong> 2. </strong> Descargar el proyecto desde el repositorio de github. <br>
          <strong> git clone https://github.com/Eliza23/Jaguar_backend.git </strong>
      </p>
    
</section>

<section class="m-5">
   <h3> Crear lista de dependencia</h3>
    <p> <strong> 1. </strong> Instalar dependencias. </br>
	    <strong>  pip install nombre_paquete. </strong> </p>
   <p> <strong> 2. </strong> Ver dependencias instalados. </br>
	   <strong>  pip freeze </strong> </p>
   <p> <strong> 3. </strong>  Crear elarchivo con la lista de dependencias. </br>
	<strong> pip freeze > requeriments.txt </strong> </p>
    <p> <strong> 4. </strong> Instalar la lista de dependencias del proyecto. </br>
	<strong> pip install -r requeriments.txt </strong> </p>
</section>


<section class="m-5">
   <h3> Empaquetar proyecto DJANGO</h3>
   <p> <strong> 1. </strong> Crear el proyecto con DJango (jaguar-backend) </p>
	<p> <strong> 2. </strong> Copiar el proyecto en una carpeta (jaguar_backend_dist) </p>
	<p> <strong> 3. </strong> Dentro de la nueva carpeta, crear los archivos LICENCE, pyproyect.toml, README.md y setup.py </p>
   <p> <strong> 4. </strong> Copiar contenido en cada archivo.</br>
   <strong> 4.1 </strong>  En el archivo pyproyect.toml </br>
      [build-system] </br>
      requires = ["setuptools>=42"] </br>
      build-backend = "setuptools.build_meta" </br>
   <strong> 4.2 </strong>  En el archivo setup.py  </br>
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

   <p> <strong> 5. </strong> Ejecutar los comandos para generar los paquetes de distribucion: </br>
	<strong> py -m pip install --upgrade build </strong> </br>
	<strong> py -m build </strong></p>
   <p> <strong> 6. </strong> Esto generara una nueva carpeta llamada dist que tiene 2 archivos: </br>
	      El tar.gzq que es un archivo fuente y el .whl es una distribución construida. </br>
            dist/</br>
               example-package-YOUR-USERNAME-HERE-0.0.1-py3-none-any.whl</br>
               example-package-YOUR-USERNAME-HERE-0.0.1.tar.gz </p>
   <p> <strong> 7. </strong> Instalar el proyecto </br> 
   <p> <strong> 7.1 </strong> Descompirmir el archivo .tar.gz </br> 
   <p> <strong> 7.2 </strong> Ejecutar el comando python setup.py install </p>
</section>

