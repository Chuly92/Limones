## Método GET

### 1. Listar todos los productos

* #### URL

> ##### /products

* #### Params

> ##### Required: NONE
  
* #### Success Response

> ##### Code: 200 
> ##### Content: { code : 1, name : "Embrague Sachs", price : 2000.00, stock : 15 }

* #### Error Response

> ##### Code: 404 NOT FOUND 

> ##### Content: { error : "No se encontraron productos " }

> ##### Code: 408 REQUEST TIMEOUT 

> ##### Content: { error : "Sitio momentáneamente no disponible. Por favor reintente en unos instantes." }

----------------------------------------------------------------------------------------------------------

### 2. Listar un producto específico por código

* #### URL

> ##### /products/:code

* #### Params

> ##### Required: code=[integer] 
  
* #### Success Response

> ##### Code: 200 
> ##### Content: { code : 1, name : "Embrague Sachs", price : 2000.00, stock : 15 }

* #### Error Response

> ##### Code: 404 NOT FOUND 

> ##### Content: { error : "La página web solicitada no se encuentra disponible actualmente." }

> ##### Code: 408 REQUEST TIMEOUT 

> ##### Content: { error : "Sitio momentáneamente no disponible. Por favor reintente en unos instantes." }

----------------------------------------------------------------------------------------------------------

