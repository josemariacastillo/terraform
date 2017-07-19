# Ficheros de Configuración

El lenguaje de los ficheros de configuración de Terraform se llama HashiCorp Configuration Language (HCL). Los ficheros se deberán crear con la extensión “.tf”.

Ejemplo de fichero Terraform, en el cual nos conectamos a la base de datos Mysql y creamos una base de datos llamada terraformbbdd.
```bash
# nano /home/usuario/terraform_example/mysql_create.tf

# Configuracion the MySQL server
provider "mysql" {
  endpoint = "localhost:3306"
  username = "root"
  password = "root"
}

# Crear base de datos
resource "mysql_database" "app" {
  name = "terraformbbdd"
}
```

### Opciones básicas:
- Los comentarios de una sola línea comienzan con #
- Los comentarios de varias líneas se envuelven con /* y */
- Los valores se asignan con la sintaxis key = value (el espacio en blanco no importa). El valor puede ser cadena, número, booleano, una lista o un diccionario.
- Las cadenas están en comillas dobles.
- Las cadenas pueden tomar otros valores usando la sintaxis envuelta en ${} , como ${var.foo}. 
- Las cadenas de multilínea pueden usar la sintaxis de "aquí doc", con la cadena comenzando con un marcador como <<EOF y luego la cadena que termina con EOF en una línea propia. Las líneas de la cadena y el marcador final no deben estar sangrados.
- Se supone que los números son la base 10. Si se prefiere un número con 0x , se trata como un número hexadecimal.
- Valores booleanos: true , false .
- Las listas de tipos primitivos se pueden hacer con corchetes ( [] ). Ejemplo: ["foo", "bar", "baz"] .
- Los diccionarios se pueden hacer con llaves ( {} ) y dos puntos (:): { "foo": "bar", "bar": "baz" } . Las citas pueden omitirse en las teclas, a menos que la clave comience con un número, en cuyo caso se requieren comillas. Se requieren comas entre pares clave / valor para diccionarios de una sola línea.

Terraform también admite los archivos de configuración con formato json. Aquí tenemos el mismo ejemplo que utilizamos arriba. Los ficheros Terraform con este formato se crearan con la extensión “.tf.json”.

```bash
# nano /home/usuario/terraform_example/mysql_create.tf.json

{

  "provider" :   {
    "mysql" :   {
      "endpoint" : "localhost:3306" ,
      "username" : "root" ,
      "password" : "root"
  }
 },

   "resource" :   {
     "mysql_database" :   {
       "app" :  {
         "name" : "terraformbbdd"
    }
   }
  }
}

```

