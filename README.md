# How to customize developer portal in Azure API Management 
Do you know that Azure API management service handles more than 77 billion API request each month and that number of API requests is doubling every 6 months?

Do you know how easy it can be to publish, manage, secure and analyze you APIs in minutes using Azure API Management?

Do you know that with Azure API management service you can take any backend system, hosted across different service or platforms, and expose it to internal and external developers through a modern API gateway?

With the power of Azure API management, it is easy to become a digital enterprise, monetize your existing data and services, and open new channel to new customers. Start publishing your APIs, make them available to internal and external developers. To release innovation, and to grow your market share, whether you are a startup or large enterprise, it’s time to join the API economy. Before we dive into the customizing of developer portal, we would like to give a brief introduction of what is Azure API management. 

## Before you start  - prerequisite:
1.	Create a Azure API Management service instance in your Azure portal

2.	Add a product: Before you can publish an API, you need to add it to a product, which contains one or more APIs and constraints such as a usage quota and term of use. 

3.	Import or create a new API

4.	Publish your product to make your API available.

## How to customize the Developer Portal
### Customize the layout of pages in Publisher Portal
Before we start customizing the whole developer portal, the first thing we can do is to structure the layout of every page which consists of a set of small page elements known as “widgets”. To structure the layout, open the API Management Service you created in the Azure portal, click “Publisher Portal”:

![1](https://iconfinastra.blob.core.windows.net/docimage/1.png)

In publisher portal, select “Widget”:

![2](https://iconfinastra.blob.core.windows.net/docimage/2.png)

As shown in the right side of the widgets page, here you can create, edit and delete any widgets as you like. 

![3](https://iconfinastra.blob.core.windows.net/docimage/3.png)

Among all the components, “Content” is the one where the core content of each webpage in your developer portal resides. All the other layout elements belongs to the rest of the widgets. Meanwhile, these widgets will be applied to every page inside your developer portal, which means that any revision you made to a widget will show changes to all the pages.

For example, if you want to create a header widget to your website including your company name and icon:
Click “add” in the header widget:

![4](https://iconfinastra.blob.core.windows.net/docimage/4.png)

In the “edit widget” page, fill in the “Title” blank with a name (this is just the name for this widget, be sure to uncheck the “Check to render the title on the front-end, uncheck to hide” box if you don’t want to show the name of the widget in the developer portal). 

In the “Body” box , enter the html codes which is used to customized the header. As an example html sentence shown in the picture below, once we saved the modification, a company logo will be shown in the header of each webpage. 

![5](https://iconfinastra.blob.core.windows.net/docimage/5.png)

![6](https://iconfinastra.blob.core.windows.net/docimage/6.png)

### Modify the content of webpage in Developer Portal
In the API Management service you created in Azure portal, select “Overview”. Then click “Developer Portal” on the top of this window, this allows you login to the developer portal with the administrator credential hence you can customize the details of each webpage.  If you choose to click the “developer portal url” link, you will log into the portal as a guest and will not have the authorization to modify the content. 

![7](https://iconfinastra.blob.core.windows.net/docimage/7.png)

To modify the content, click the icon on the left which is represented by two brushes. 

![8](https://iconfinastra.blob.core.windows.net/docimage/8.png)

### Customize the style of pages in Developer Portal
Open the customizing panel by click the icon as shown in the previous content, select “Styles” to enter into styling customizing section:

![9](https://iconfinastra.blob.core.windows.net/docimage/9.png)

“Styles” section is the place where you can customize all the style elements such as background color, text color, fonts, text size, padding and margin, without writing actual code using html or CSS. You can easily change the property of any elements just by inputting a new value to the corresponding parameter box. 

For example, if you want to change the color of heading text,  enter "headings" in the “Change variable values to customize developer portal appearance” field and change “

![10](https://iconfinastra.blob.core.windows.net/docimage/10.png)

By clicking the “headings-color”, the drop-down box gives you a picker to find the color you want, or you can also simply input the value of the color. 

![11](https://iconfinastra.blob.core.windows.net/docimage/11.png)

If you are not sure about which parameter is the one you want to change to modify the corresponding element, select “Select an element on the page” button and the parameters related to the area you manually selected will be automatically displayed in the “Style” panel. As shown in the image below, here we select “Products” area in the footer:

![12](https://iconfinastra.blob.core.windows.net/docimage/12.png)

The “Style” panel will display the related parameters:


![13](https://iconfinastra.blob.core.windows.net/docimage/13.png)

### Modify the templates of pages in Developer Portal
Templates are used to customize the content of system-generated pages such us “Products” and “API List” in Developer Portal. It offers you flexibility to modify the content by using DotLiquid syntax. DotLiquid is a templating system ported to the .NET framework from Ruby’s Liquid Markup.

#### Templates Overview
In the list shown in “Templates” panel, different templates have been categorized and each template covers a single webpage. Click the name of the template you want to modify, here we take “product list” template as an example:

![14](https://iconfinastra.blob.core.windows.net/docimage/14.png)

By clicking the name of the templates, it routes you to the corresponding webpage you want to edit and opens the template editing panel where you can change the DotLiquid syntax. 

![15](https://iconfinastra.blob.core.windows.net/docimage/15.png)

Whenever you make a change to the template, the corresponding results will be automatically shown in the content in real-time. However, the change is not visible to other clients who opened the webpage until you save and publish the modification. 

![16](https://iconfinastra.blob.core.windows.net/docimage/16.png)

As shown in the picture above, the first icon in the red bounding box is used to save a template. In order to make the changes visible for any other user, after clicking “save” button, then click “publish” button which is the second icon in the red bounding box. 

To revert the published version into the previous one, click the third button “revert”. 

To restore the template into the original default version, click the fourth button “restore”. 

The template editor consist of two different components: template customizing section and template data section. The left box is the place where you make all the changes to the syntax on top of some pre-built default syntax. The right box displays the data model for the entities that are available in this template. You cannot make any changes to the “Template data” section. 

#### Example of customized product page
Here is a screenshot of webpage generated by default “Product List” template.
![17](https://iconfinastra.blob.core.windows.net/docimage/17.png)

The screenshot below gives an example of  the webpage generated by customized Product List” template.
![18](https://iconfinastra.blob.core.windows.net/docimage/18.png)

Code:
```
<search-control></search-control>
<div class="row", sytle="margin-left:200px;">
    <div class="col-md-9">
        <h2 style="margin-left: 15px;margin-bottom: 30px;">{% localized "ProductsStrings|PageTitleProducts" %}</h2>
    </div>
</div>
<div>
    <div class="col-md-12">
	{% if products.size > 0 %}
	<div class="list-unstyled">
	
	{% for product in products %}
		<div style="width:33%;float:left">
		

		    <img src="https://iconfinastra.blob.core.windows.net/icons/{{product.id}}.png"
		    style="float:left;width:35px;height:auto">

		    <div style="float:left;">
			<p style="font-size:22px; margin-left: 10px;margin-bottom: 10px;"><a href="/products/{{product.id}}"> {{product.title}}</a></p>
			<p style="margin-left: 10px;">{{product.description}}</p>
			</div>
		</div>
	{% endfor %}
	
	</div>
	<paging-control></paging-control>
	{% else %}
	{% localized "CommonResources|NoItemsToDisplay" %}
	{% endif %}
	</div>
</div>
```

#### Example of customized API List page
Here is a screenshot of webpage generated by default “Product” template.
![19](https://iconfinastra.blob.core.windows.net/docimage/19.png)

The screenshot below gives an example of the webpage generated by customized “Product” template.
![20](https://iconfinastra.blob.core.windows.net/docimage/20.png)

```
<style>
table {
    font-family: arial, sans-serif;
    table-layout: fixed;
    border-collapse: collapse;
    width: 100%;
    text-align: middle;
    vertical-align: middle;    
}

td, th{
    border: 1px solid #dddddd;
    text-align: middle;
    padding: 8px;

}


</style>

<img src="https://iconfinastra.blob.core.windows.net/icons/{{product.id}}.png"
		    style="float:left; margin-right: 10px;margin-bottom: 5px; margin-top: 5px; width:40px;height:auto">
<h2>{{Product.Title}}</h2>

<!--count the number of APIs-->
{% assign replaceString0 = '{0}' %}

{% if Limits and Limits.size > 0 %}
<h3>{% localized "ProductDetailsStrings|WebProductsUsageLimitsHeader"%}</h3>
<ul>
  {% for limit in Limits %}
  <li>{{limit.DisplayName}}</li>
  {% endfor %}
</ul>
{% endif %}
<!--count the number of APIs-->


<!--This product contains apis.size API:-->
{% if apis.size > 0 %}
<p>
  <b>
    {% if apis.size == 1 %}
    {% capture apisCountText %}{% localized "ProductDetailsStrings|TextblockSingleApisCount" %}{% endcapture %}
    {% else %}
    {% capture apisCountText %}{% localized "ProductDetailsStrings|TextblockMultipleApisCount" %}{% endcapture %}
    {% endif %}

    {% capture apisCount %}{{apis.size}}{% endcapture %}
    {{ apisCountText | split : replaceString0 | join : apisCount }}
  </b>
</p>
<!--This product contains apis.size API:-->




<!--my table-->
<table>

  <tr>
{% for api in Apis %}
  <th>

   <center>
   <div style="color:#007ca6;  font-size:22px; "><p >{{api.Name}}</p></div>
   <p><img src="https://iconfinastra.blob.core.windows.net/elements/{{api.Id}}.png" style="float:middle;width:200px;height:auto"></p>
   <p style="margin-left: 10px;">{{api.description}}</p>
   <p><a href="/docs/services/{{api.Id}}">See Details</a></p>
   </center>
  </th>
  {% endfor %}
  </tr>
</table>

  
{% endif %}

{% if subscriptions.size > 0 %}
<p>
  <b>
    {% if subscriptions.size == 1 %}
    {% capture subscriptionsCountText %}{% localized "ProductDetailsStrings|TextblockSingleSubscriptionsCount" %}{% endcapture %}
    {% else %}
    {% capture subscriptionsCountText %}{% localized "ProductDetailsStrings|TextblockMultipleSubscriptionsCount" %}{% endcapture %}
    {% endif %}

    {% capture subscriptionsCount %}{{subscriptions.size}}{% endcapture %}
    {{ subscriptionsCountText | split : replaceString0 | join : subscriptionsCount }}
  </b>
</p>


<div style="margin-bottom: 20px;" >
  {% for subscription in subscriptions %}
<input class="btn" type="button"  value="{{subscription.DisplayName}}" onclick="window.location.href='/developer#{{subscription.Id}}'" />
  {% endfor %}
  </div>




{% endif %}
{% if CannotAddBecauseSubscriptionNumberLimitReached %}
<b>{% localized "ProductDetailsStrings|TextblockSubscriptionLimitReached" %}</b>
{% elsif CannotAddBecauseMultipleSubscriptionsNotAllowed == false %}
<subscribe-button></subscribe-button>
{% endif %}
```
