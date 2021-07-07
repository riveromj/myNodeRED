# myNodeRED
# exampleNodeRED
how to create a custom node
1. Arrancar nodeRED dentro de un contenedo docker
    creamos una carpeta para el contenedor
    entramos en la carpeta y ejecutamos el comando > docker run --name <nombreContenedor> -p 1880:1880 -v <ruta local del contenedor>:/data <nombre de la imagen>
        docker run --name mynodered -p 180:1880 -v <ruta local del contenedor>:/data nodered/node-red

2. http://localhost:1880/ ya tenemos crriendo el contenedor
  
3. Entramos en la carpeta node_modules y creamos la carpeta del nodo la cual debe contener 3 archivos .js - .html y package.json
  (ver documentación https://nodered.org/docs/creating-nodes/first-node)
     package.json: en nombre del nodo, node-red y donde esta definido el nodo archivo.js
    archivo.js: definir en nodo con una funcion
    archivo.html: tiene 3 partes: 
      1. inicialización de  javascript
      2. el formulario que se muestra en el editor para conficurar el nodo
      3. la ayuda que se mostrara en el     editor para explicar lo que hace el nodo.
  
  4. reiniciamos el contenedor y ya debemos ver el nodo nuevo en nodeRED
