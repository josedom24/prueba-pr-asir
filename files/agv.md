<h2>¿Qué asignatura te gusta más?</h2>
1. **FOL**
2. **IWEB**

<h2>¿Por qué?</h2>

		1. Porque la tengo convalidada y puedo echarme una siestecita de una hora en casa
		2. Porque me mola la páginita que hice el año pasado con su script que sube los cambios solos a github:

		read -p "¿Has añadido archivos nuevos? (y/n) " nuevos
		read -p "¿Cual va a ser el commit? " comentario

		if [ $nuevos == "y" ]
		    then
		    cd blog_hugo/
		    git add .
		    git commit -am "$comentario"
		    git push
		    hugo -d  ../alepeteporico.github.io/
		    cd ../alepeteporico.github.io/
		    git add .
		    git commit -am "$comentario"
		    git push
	
		elif [ $nuevos == "n" ]
		    then
		    cd blog_hugo/
		    git commit -am "$comentario"
		    git push
		    hugo -d  ../alepeteporico.github.io/
		    cd ../alepeteporico.github.io/
		    git commit -am "$comentario"
		    git push

		fi

