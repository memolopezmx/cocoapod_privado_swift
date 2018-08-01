Crear un Pod privado
===

Nos otros a lo largo de nuestra carrera como desarrolladores vamos creando diversas funciones de código, código que podemos re-implementar en futuros proyectos. Podemos conservar este código en librerías (frameworks para Swift), Cocoa Pods no es más que subir nuestras librerías a repositorios publicos o privados y posteriormente implementarlos de una manera simple en nuestro proyecto desde esos repositorios.

## Requisito

Como requerimiento debemos tener nuestra claseo o clases con el código que queremos guardar en la librería y subir al pod. Para este ejemplo yo usaré un código de cifrado.

## 1. Creamos un repositorio

Para este usaremos <a href="https://gitlab.com/">Gitlab</a> pero podemos usar BitBucket o cualquier otro.

<p>
	<img src="imgs/img1.png" width="" height="">
</p>

<p>
	<img src="imgs/img2.png" width="" height="">
</p>

<p>
	<img src="imgs/img3.png" width="" height="">
</p>

## 2. Creamos un framework en Xcode

Creamos un framework adaptando nuestra funcionalidad para que se pueda usar instanciando una clase o llamando a un método de esa clase. En mi caso creare una nueva clase y agregare las funciones a esta.

<p>
	<img src="imgs/img4.png" width="" height="">
</p>

<p>
	<img src="imgs/img5.png" width="" height="">
</p>

<p>
	<img src="imgs/img6.png" width="" height="">
</p>

En mi caso la clase se llama igual que el framework pero puede variar.

<p>
	<img src="imgs/img7.png" width="" height="">
</p>

<p>
	<img src="imgs/img8.png" width="" height="">
</p>

Implementamos todo lo necesario.

## 3. Subimos el framework al repositorio.

```
> cd existing_folder
> git init
> git remote add origin url_repo.git
> git add .
> git commit -m "Initial commit"
> git push -u origin master
```

Hay un punto importante para un mejor ordenamiento manejaremos el versionado de nuestro pod con **tags**. Así cada vez que hagamos cambios deberemos subirlos con un *git push* normal y posteriormente hacer un tag con un versionado y de nuevo haremos un *git push* pero con tags.

```
git tag 0.0.1
git push origin master --tags
```



## 4. Creamos el archivo de configuración podspect






