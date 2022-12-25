# Notas para RestApi

### Generar Token

> Cuando estaba intentando generar el Token de Acceso producía un error:
> 									 [*Expired authorization code and Invalid Nonce errors*](https://salesforce.stackexchange.com/questions/261547/expired-authorization-code-and-invalid-nonce-errors)
>
> Esto parecía producirse porque:
>
> 1. Tenía abiertas dos instancias de **Postman**
> 2. No estaba activado el allow cors en la parte de **CORS configuration** en la org
> 3. No tener activados **Pop-ups** en el navegador



------



### Recibir respuesta XML

> Al parecer aunque la documentación de salesforce dice que para recibir una respuesta **XML** en la RESTapi es solo necesario cambiar el header *Content-Type* a *Application/xml*, al parecer **ES NECESARIO** cambiar el header *Accept* a 
>
> *Application/xml*.



------



### Nota con respecto a redirecciones

> Es posible que cuando un request haga una redirección no se mantenga el *header de autenticación* por lo que es necesario activar esa opción en **Postman**