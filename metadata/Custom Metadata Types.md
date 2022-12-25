# Get Started with Custom Metadata Types

> ### ***Metadata is data that describes other data.*** 
>
> When you add a record with a customer’s contact information to an Account, you are adding metadata and data.
>
> Field names, such as *first name* and *last name* are metadata. The values in those fields, for example, *Amy* and *Lane* are data.

A *custom metadata type* is an object that is **used to define the structure for application metadata**.

> Using metadata is pretty handy because it can be imported into Salesforce, modified in the interface, and manipulated using the *Metadata API*. 

## Deploy metadata types

> When you deploy apps with custom metadata types, all of the records and fields are included in the package installation, so no additional steps are needed. 
>
> You can **deploy** custom metadata types from a sandbox with *change sets* or *packaged in managed packages*.

Unlike custom metadata types, when you deploy apps with custom objects and custom settings, the metadata for those objects (the header) gets deployed, but the records (definitions) are left behind. 



Whether you’re manually loading records or inserting records using an Apex script, adding records can be a time-consuming process. 



Here are some examples of what you can do with custom metadata types.

- **Mappings**—You can use custom metadata types to create associations between different objects. I.E you can create a custom metadata type that assigns cities, states, or provinces to particular regions in a country.
- **Business rules**—Salesforce has lots of ways to define business rules. One way is to combine configuration records with custom functionality. For example, you can use custom metadata types along with some Apex code to route payments to the correct endpoint.
- **Master data**—Say that your org uses a standard accounting app. You can create a custom metadata type that defines custom charges, like duties and VAT rates. If you include this type as part of an extension package, subscriber orgs can reference this master data.
- **Protected information**—Store data like API keys in a protected package.



## More About Custom Metadata Types

Custom metadata types support most standard field types, including:

- Metadata Relationships
- Checkbox
- Date and Date/Time
- Email and Phone
- Number
- Percent
- Picklist
- Text and Text Area
- URL

### **Developer Support**

Developers can use SOQL to read custom metadata types. To create or update metadata records, they can use the Metadata API. Apex code can create, read, and update (but not delete) custom metadata records.

### **Reference Custom Metadata Types**

Custom metadata types can be used directly from:

- Apex
- Flows
- Formula fields
- Validation rules

Custom metadata types are customizable, deployable, packageable, and upgradeable application metadata. In many cases, custom metadata types have an advantage over custom settings and custom objects. They can make your application lifecycle management and compliance easier, faster, and more robust. In the next unit, you create your own custom metadata type.

*Answer* : MasterData

![image-20221222015401819](/home/teo/.config/Typora/typora-user-images/image-20221222015401819.png)