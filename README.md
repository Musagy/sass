### comemzamos curso de Sass :)
primero comenzaremos con la instalacion del npm con 
        
        npm install -g node-sass

despues de eso ya en la carpeda tendremos que usar el terminal para automatizar el compilado de sass a css

tenemos que poner
        
        node-sass --watch (carpera de sass) --output (carpeta donde copilara)


## declaracion de variables
ahora ya que tenemos todo listo comenzemos declarando variables:

        $variable: #fff;

- se hacen con $ y he notado que no aceptan camelCase o no se pero me da errores asi que voy a usar guiones.

para su aplicacion es poner lo mismo cuando la declaramos

        h1{
            color: $variable;
        }
    
con estas podremos poner hacer operacione sin el uso de calc()

        h1{
            font-size: $variable-numerica - 20px;
        }

si $variable-numerica es de 30px terminara como resultado 10px

## !default
esta propiedad le dira a la variable que esta sera la propiedad por defecto, o sea que esta declaracion solo va a servir si es que no se ha declarado o sobreescrito

        $bg-color: rgb(255, 231, 218) ;
        $bg-color: rgb(0, 0, 0) !default;

        body{
            background-color: $bg-color;
        }

## variables como selectores
las variables sass tambien las variables pueden funcionar como string poniendolas entre #{}
               
        $color: red;

        .#{$color} {
            color: $color;
        }

- en este caso al poner un punto al inicio del #{} lo imprime como si fuera clase, porque las clases se ponen con un . al principio
