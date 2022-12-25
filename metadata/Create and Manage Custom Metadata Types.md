# Create and Manage Custom Metadata Types

Check the trailhead for creating MetadataTypes and adding new records:

***[Metadata Type and record creation](https://trailhead.salesforce.com/es-MX/content/learn/modules/custom_metadata_types_dec/cmt_create?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-platform-developer-ii-credential)***



> *Hay que entender que una de las principales razones para usar metadatatypes en su caracter como información*
>
> *que tiene a permanecer estática, podríamos usar sin problemas objectos normales y nos funcionarían de igual*
>
> *manera, con la excepción de que no podríamos intercambiarlos entre organizaciones de manera sencilla*
>
> 
>
> Por ende en el ejemplo podemos comprender porqué quisiera tal vez importar todos los **records** creados de metadato **VAT Data**(IVA)  porque quisiera exportar a distintas organizaciones mis listas de países con los respectivos datos de su IVA.



------



# Use Custom Metadata Types in Formulas, Default Values, and Validation Rules



> Los tres usos más importantes de los metadatos son en formulas, default values y validation-rules
>
> - *default values*: como era de esperarse tener una lista de objetos de una lista de posibilidades es un buen uso de los metadatos, entonces si quiero agregar un nuevo object X, puedo hacer que uno de sus campos sea una referencia a alguno de la lista de los metadatos.
> - *validation rules*: Las validaciones se realizan antes de guardar un objeto, si tengo que mi lista de **default values** da opciones que tal vez debería de cumplir ciertos requisitos puedo puedo mandar mensajes de error através de una validation rule.
> - *formulas*: Las formulas nos permiten agregar información extra sobre el metadato y procesar la información quee tenemos de él.

checar el [trailhead para este tema](https://trailhead.salesforce.com/es-MX/content/learn/modules/custom_metadata_types_dec/cmt_formulas?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-platform-developer-ii-credential) & el tema de *Metadata in Flows*



## Resources

- *Salesforce Help*: [Reference Custom Metadata Type Records in Default Values](https://help.salesforce.com/articleView?id=custommetadatatypes_default_fields.htm&language=en_US)
- *Salesforce Help*: [Custom Metadata Type Fields and Validation Rules](https://help.salesforce.com/articleView?id=custommetadatatypes_field_validation.htm&language=en_US)
- *Salesforce Help*: [Custom Metadata Types and Advanced Formula Fields](https://help.salesforce.com/articleView?id=custommetadatatypes_formula_fields.htm&language=en_US)