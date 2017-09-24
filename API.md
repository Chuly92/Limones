## Método GET

### 1. Listar todos los productos

* #### URL

> ##### /products/list

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

### 2. Listar un producto específico por código

* #### URL

> ##### /products/list/:code

* #### Params

> ##### Required: code=[integer] 
  
* #### Success Response

> ##### Code: 200 
> ##### Content: { code : 1, name : "Embrague Sachs", price : 2000.00, stock : 15 }

* #### Error Response

> ##### Code: 404 NOT FOUND 

> ##### Content: { error : "No hay datos para el código de producto solicitado." }

> ##### Code: 408 REQUEST TIMEOUT 

> ##### Content: { error : "Sitio momentáneamente no disponible. Por favor reintente en unos instantes." }

----------------------------------------------------------------------------------------------------------

### 3. Listar un producto específico por nombre

* #### URL

> ##### /products/list/:name

* #### Params

> ##### Required: name=[string] 
  
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

> ##### /products/new_product

* #### Params

> ##### Required: code=[integer], name=[string], price=[decimal], stock=[integer]  
  
* #### Success Response

> ##### Code: 201 
> ##### Content: { "Su producto ha sido dado de alta exitósamente en la base de datos." }

* #### Error Response

> ##### Code: 422 UNPROCESSABLE ENTITY

> ##### Content: { error : "No se pudo realizar el alta del producto solicitado." }

> ##### Code: 408 REQUEST TIMEOUT 

> ##### Content: { error : "Sitio momentáneamente no disponible. Por favor reintente en unos instantes." }

----------------------------------------------------------------------------------------------------------

## Método PUT

### 1. Modificación del stock del producto

* #### URL

> ##### /products/alter_stock

* #### Params

> ##### Required: code=[integer], stock=[integer]  
  
* #### Success Response

> ##### Code: 200 
> ##### Content: { "Su producto ha sido modificado exitósamente." }

* #### Error Response

> ##### Code: 422 UNPROCESSABLE ENTITY

> ##### Content: { error : "No se pudo realizar la modificación del producto solicitado." }

> ##### Code: 408 REQUEST TIMEOUT 

> ##### Content: { error : "Sitio momentáneamente no disponible. Por favor reintente en unos instantes." }

----------------------------------------------------------------------------------------------------------

### 2. Modificación del precio del producto

* #### URL

> ##### /products/alter_price

* #### Params

> ##### Required: code=[integer], price=[decimal]  
  
* #### Success Response

> ##### Code: 200 
> ##### Content: { "Su producto ha sido modificado exitósamente." }

* #### Error Response

> ##### Code: 422 UNPROCESSABLE ENTITY

> ##### Content: { error : "No se pudo realizar la modificación del producto solicitado." }

> ##### Code: 408 REQUEST TIMEOUT 

> ##### Content: { error : "Sitio momentáneamente no disponible. Por favor reintente en unos instantes." }

----------------------------------------------------------------------------------------------------------

## Método DELETE

### 1. Baja de producto específico

* #### URL

> ##### /products/delete_product

* #### Params

> ##### Required: code=[integer] 
  
* #### Success Response

> ##### Code: 200 
> ##### Content: { "Su producto ha sido eliminado exitósamente." }

* #### Error Response

> ##### Code: 422 UNPROCESSABLE ENTITY

> ##### Content: { error : "No se pudo realizar la eliminación del producto solicitado." }

> ##### Code: 408 REQUEST TIMEOUT 

> ##### Content: { error : "Sitio momentáneamente no disponible. Por favor reintente en unos instantes." }

----------------------------------------------------------------------------------------------------------
