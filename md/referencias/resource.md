# Carpeta `resource`

Contiene los recursos de un determinado módulo.

```txt
API
  ├─ resources
        └─ api
              └─ v1
                    └─ personas
                          ├─ persona.controller.js
                          ├─ persona.input.js
                          ├─ persona.middleware.js
                          ├─ persona.output.js
                          └─ persona.route.js
```

## Flujo de una petición

Una ruta `ROUTE` recibe los datos de entrada `INPUT`, verifica que la información proporcionada sea válida y suficiente para continuar con el proceso `MIDDLEWARE`, realiza las tareas correspondientes `CONTROLLER` y finalmente devuelve el resultado `OUTPUT`.

```txt
┌───────────┐     ┌───────────┐     ┌────────────┐     ┌────────────┐     ┌────────────┐
│   ROUTE   │ --> │   INPUT   │ --> │ MIDDLEWARE │ --> │ CONTROLLER │ --> │   OUTPUT   │
└───────────┘     └───────────┘     └────────────┘     └────────────┘     └────────────┘
```

Todo este flujo se describe en varios archivos cuya extensión define el estado en el que se encuentra. Por ejemplo, para el recurso `libros` se tendrían los siguientes archivos:

```txt
libros
   ├─ libros.controller.js
   ├─ libros.input.js
   ├─ libros.middleware.js
   ├─ libros.output.js
   └─ libros.route.js
```

Cada archivo contiene un objeto cuyas propiedades son las claves `KEY` asociadas a una ruta.

- [Archivo *.controller.js](./referencias/controller)
- [Archivo *.input.js](./referencias/input)
- [Archivo *.middleware.js](./referencias/middleware)
- [Archivo *.output.js](./referencias/output)
- [Archivo *.route.js](./referencias/route)