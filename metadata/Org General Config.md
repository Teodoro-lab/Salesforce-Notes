# Configuración de toda la organización



## Multiple currency settings

<p>In Salesforce, you can specify which currencies your organization uses, and individual users can apply specific currencies to their settings based on where they do business. </p>

Salesforce organizations use a **single currency**. Once you set the required currency locale in your company settings, *all currency values on records display in that currency.*

> But after being acquired by the Nacho Secrets Agency, Mom & Pop’s began to take on an international clientele. It was time to move from a single to a multicurrency setup.

once a multicurrency setup is enabled, *it can’t be disabled.*



As the admin for your organization, you set that “corporate currency,” which reflects the currency of your corporate headquarters. You also maintain the **list of active currencies** and their **conversion rates** relative to the corporate currency.



![image-20221222011448106](/home/teo/.config/Typora/typora-user-images/image-20221222011448106.png)



------



## Conversion Rates

![image-20221222011554656](/home/teo/.config/Typora/typora-user-images/image-20221222011554656.png)



------





## Implement Advanced Currency Management

Advanced Currency Management for currency fields on opportunities and opportunity products lets you **manage exchange rate start dates**.



Let’s check out an example:

- On January 1, you update the exchange rate to **1 USD = 0.9464 EUR**.
- On February 1, you change the exchange rate to **1 USD = 0.9353 EUR**.



| Opportunities that close...      | Use this rate...                        |
| -------------------------------- | --------------------------------------- |
| Between January 1 and February 1 | The first exchange rate (*1 = 0.9464*)  |
| After February 1                 | The second exchange rate (*1 = 0.9353*) |



------



## Add Personal Currencies

> Since Pop is devoting all his time to a long-term, top-secret case for a client in Luxembourg, he sets his currency to EUR-Euro so his transactions are reported in euros. Meanwhile, Mom does clandestine work for clients in multiple countries, so she leaves the currency on her personal settings page as USD-U.S. Dollar and manages each account’s currency individually.
>
> 
>
> ![image-20221222011954886](/home/teo/.config/Typora/typora-user-images/image-20221222011954886.png)
>
> 



