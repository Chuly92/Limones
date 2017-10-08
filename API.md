## Método GET

### 1. Lista de todos los productos paginada

* #### URL

> ##### /products

* #### Params

> ##### Required: NONE
  
* #### Success Response

> ##### Code: 200 
> ##### Content: { code : 1, name : "Embrague Sachs", price : 2000.00, stock : 15 }

* #### Error Response

> ##### Code: 404 NOT FOUND 

> ##### Content: { error : "No se encontraron productos para la búsqueda solicitada." }

> ##### Code: 408 REQUEST TIMEOUT 

> ##### Content: { error : "Sitio momentáneamente no disponible. Por favor reintente en unos instantes." }

----------------------------------------------------------------------------------------------------------

### 2. Listar un producto específico por código o nombre

* #### URL

> ##### /products/X

* #### Params

> ##### Required: code=[integer] | OR | name=[string]
  
* #### Success Response

> ##### Code: 200 
> ##### Content: { code : 1, name : "Embrague Sachs", price : 2000.00, stock : 15 }

* #### Error Response

> ##### Code: 404 NOT FOUND 

> ##### Content: { error : "No hay datos para el producto solicitado." }

> ##### Code: 408 REQUEST TIMEOUT 

> ##### Content: { error : "Sitio momentáneamente no disponible. Por favor reintente en unos instantes." }

----------------------------------------------------------------------------------------------------------

## Método POST

### 1. Alta de producto

* #### URL

> ##### /products

* #### Params

> ##### Required: code=[integer], name=[string], price=[decimal], stock=[integer]  
  
* #### Success Response

> ##### Code: 201 
> ##### Content: { "Su producto ha sido dado de alta exitósamente en la base de datos." }

* #### Error Response

> ##### Code: 405 INVALID INPUT

> ##### Content: { error : "Los datos ingresádos no son válidos o faltan campos a completar. Favor de verificar." }

> ##### Code: 408 REQUEST TIMEOUT 

> ##### Content: { error : "Sitio momentáneamente no disponible. Por favor reintente en unos instantes." }

> ##### Code: 422 UNPROCESSABLE ENTITY

> ##### Content: { error : "No se pudo realizar el alta del producto solicitado." }

----------------------------------------------------------------------------------------------------------

## Método PUT

### 1. Modificación de datos de un producto

* #### URL

> ##### /products/X

* #### Params

> ##### Required: code=[integer], stock=[integer]  

> ##### Optional: name=[string], price=[decimal], stock=[integer]    
  
* #### Success Response

> ##### Code: 200 
> ##### Content: { "Su producto ha sido modificado exitósamente." }

* #### Error Response

> ##### Code: 404 NOT FOUND 

> ##### Content: { error : "No hay datos para el producto solicitado." }

> ##### Code: 408 REQUEST TIMEOUT 

> ##### Content: { error : "Sitio momentáneamente no disponible. Por favor reintente en unos instantes." }

> ##### Code: 422 UNPROCESSABLE ENTITY

> ##### Content: { error : "No se pudo realizar la modificación del producto solicitado." }


----------------------------------------------------------------------------------------------------------

## Método DELETE

### 1. Baja de producto específico

* #### URL

> ##### /products/X

* #### Params

> ##### Required: code=[integer] 
  
* #### Success Response

> ##### Code: 200 
> ##### Content: { "Su producto ha sido eliminado exitósamente." }

* #### Error Response

> ##### Code: 404 NOT FOUND 

> ##### Content: { error : "No hay datos para el producto solicitado." }

> ##### Code: 408 REQUEST TIMEOUT 

> ##### Content: { error : "Sitio momentáneamente no disponible. Por favor reintente en unos instantes." }

> ##### Code: 422 UNPROCESSABLE ENTITY

> ##### Content: { error : "No se pudo realizar la eliminación del producto solicitado." }

----------------------------------------------------------------------------------------------------------
