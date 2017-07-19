# Características

### Infraestructura como Código

La infraestructura se describe utilizando una sintaxis de configuración de alto nivel. Esto permite que un modelo de su centro de datos sea versionado y tratado como lo haría con cualquier otro código. Además, la infraestructura puede ser compartida y reutilizada.



### Planes de Ejecución

Terraform tiene un paso de "planificación" donde genera un plan de ejecución . El plan de ejecución muestra lo que hará cuando ejecutemos terraform plan. Esto le permite evitar sorpresas cuando Terraform manipule la infraestructura.
Por ejemplo, después de crear un servidor web, podemos cambiar el tamaño de la memoria RAM del servidor de DigitalOcean. El símbolo [~] antes del Droplet significa que Terraform actualizará el recurso, en lugar de destruir o recrear.
 ``` bash
$ Terraform plan
 ~ Digitalocean_droplet.web
     Tamaño: "512mb" => "1gb"

```
### Representación gráfica de recursos

Terraform construye un gráfico de todos sus recursos y paraleliza la creación y modificación de cualquier recurso no dependiente. Debido a esto, construye la infraestructura lo más eficientemente posible, y los operadores obtienen una visión sobre las dependencias en su infraestructura.

### Automatización de los cambios

Los conjuntos de cambios complejos se pueden aplicar a su infraestructura con una mínima interacción humana. Con el plan de ejecución y el gráfico de recursos antes mencionados, usted sabe exactamente lo que cambiará Terraform y en qué orden, evitando muchos posibles errores humanos.








