MultilingualPress is built to perfectly integrate with the WooCommerce environment. And hence it can also properly connect and translate the WooCommerce Attributes.

Let's check how this works in this brief tutorial.

## Create an attribute, an example

Before connecting WooCommerce attributes in MultilingualPress, we first need to create one.

So, let's create an attribute in our WordPress Multisite Network Shops: for example we create a color attribute in the English sub site.

To achieve that we go to _Products->Attributes_ . From here we set the attribute name as _color_ and the related slug as _color_.

After that we can then configure some Terms using the _Configure Terms_ link shown in the picture below.

[caption id="attachment_14459" align="aligncenter" width="3338"][![Create WooCommerce Attributes and Terms](https://multilingualpress.org/wp-content/uploads/sites/12/2020/11/Create-WooCommerce-Attributes-and-Terms.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2020/11/Create-WooCommerce-Attributes-and-Terms.png) Create WooCommerce Attributes and Terms[/caption]

Hence we have some Terms (Blue, Gary, Green, Red, Yellow) for the _color_ attribute.

## Same attribute on different sub site: set the connection

Suppose now to set a similar attribute on another sub site, let's say a Spanish version of the English one described in the previous section.

In that case we can similarly proceed in creating an attribute, but this time the Terms will be properly translated in Spanish language.

Let's focus on the "Blue" Term. This in Spanish language is "Azul". We proceed and create this Term.

At this point we need to understand how to connect the Attribute between the two sites.

We want that the _color_ attribute in the English site is connected via MultlingualPress to the _color_ attribute in the Spanish site. To achieve that **they have to share exactly the same slug**: _color_ in this case.

As we can see the slug in the English site is _color ._

[caption id="attachment_14465" align="aligncenter" width="1856"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2020/11/WooCommerce-Attribute-in-English-language-site.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2020/11/WooCommerce-Attribute-in-English-language-site.png) WooCommerce Attribute slug in English language site set as "color"[/caption]

And similarly in the Spanish site the slug is still _color_.

[caption id="attachment_14466" align="aligncenter" width="1798"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2020/11/WooCommerce-Attribute-in-Spanish-language-site.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2020/11/WooCommerce-Attribute-in-Spanish-language-site.png) WooCommerce Attribute slug in Spanish language site set as "color"[/caption]

In the following picture we see again that the color attribute in the Spanish version site with the slug set as _color_ but we also show that the _Azul_ Term is configured.

[caption id="attachment_14468" align="aligncenter" width="2794"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2020/11/WooCommerce-Attribute-in-Spanish-site.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2020/11/WooCommerce-Attribute-in-Spanish-site.png) Create WooCommerce Attributes and Terms in Spanish language site[/caption]

## MultilingualPress attribute connection established

Now that the color WooCommerce Attributes share the same slug, it is easily possible to set the language relations of the Terms of through the translation metaboxes.

In fact, as reported in the picture below, when you edit one of the terms and search for related term in the other language site,  MultilingualPress will try to find the term within the attribute with the same slug.

In that case and will not look for term in attribute called Size for example. Instead it will check for the slug _color_ .

[caption id="attachment_14469" align="aligncenter" width="2006"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2020/11/Translation-Metabox-is-able-to-find-and-connect-the-related-Terms.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2020/11/Translation-Metabox-is-able-to-find-and-connect-the-related-Terms.png) The Translation Metabox is now able to properly find and connect the related Terms[/caption]

Filling the form with the "Az" values, will let MultilingualPress search within the English color Attribute, and retrieve the Azul Term.

If you want to know more about how to properly set your MultilingualPress environment have a look at our [Getting Started with MultilingualPress](https://multilingualpress.org/docs/getting-started-with-multilingualpress-3/) tutorial.