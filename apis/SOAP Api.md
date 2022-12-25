## Enterprise and Partner WSDLs



The **Web Services Description Language (WSDL)** file is basically your map to understanding how to use the API. It contains the bindings, protocols, and objects to make API calls.

> Salesforce provides two SOAP API WSDLs for two different use cases. The enterprise WSDL is optimized for a single Salesforce org. It’s strongly typed, and it reflects your org’s specific configuration, meaning that two enterprise WSDL files generated from two different orgs contain different information.



------



![Sample SOAP login request](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/api_basics/api_basics_soap/images/62d42aa58407088ae213fcd183c958c4_api-basics-soap-soapui-3.png)

 Quick **breakdown of the endpoint URI** (1).

- https://—Specifies secure HTTP.
- login.salesforce.com—Top-level domain for a login request.
- /services/Soap—Specifies that we’re making a SOAP API request.
- /c—Specifies that we’re using the enterprise WSDL. Use /u for the partner WSDL.
- /36.0—API version number. The v prefix is missing because some APIs include it before the version number, and some don’t. This behavior is just a quirk of Salesforce APIs.
- /0DF36000000LHZw—Package version number.



The **SOAP message** (2) contains everything we expect to find in a SOAP message: an *envelope*, a *header*, and a *body*.

In this type of request a lot of information that may be useful is added, otherwise you can deleted for the current request.



# General Notes

> Es importante que siempre se descargue el *correcto WSDL* para que no hayan fallos al momento de hacer el request. otras consideraciones incluyen el *correcto dominio* al momento de realizar el request además de haber agregado el *token de seguridad*(que se genera el la configuración local) al password.
>
> 
>
> También podríamos familiarizarnos más con la aplicación para hacer requests SOAP.

