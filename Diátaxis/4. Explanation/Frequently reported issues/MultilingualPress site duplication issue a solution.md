MultilingualPress site duplication issue: a solution

One of the is the so called "_Based on_" option. Through this option you can create a  new site as a duplication of an already existing other sub site.

Hence this feature let you to create a new sub site as a copy of another, copying also the source site content , the configurations and the translation connections.

But in a particular case one or more third party plugins could interrupt the process. Let's see what the problem is and how MultilingualPress solves it.

## Duplicate your site in one click

Suppose you have a shop in your own language, but you wish also to create a new one in another language.

The two shops should be quite similar, only languages will be different.

In that case would be much faster for you if the new site is created as a duplication of the former one. No manual settings, just get what you need in one click.

That's what you can achieve with MultilingualPress!

What you need to do is to select the "_Based on_" option on the new site creation page. For further details on this feature please have a look to our [Getting Started with MultilingualPress](https://multilingualpress.org/docs/getting-started-with-multilingualpress-3/#Create-a-new-website-within-the-multisite-and-set-the-language-for-the-site) guide.

## Duplication issue due to third party plugins redirection

Unfortunately if the source site has installed some third party plugins whose activation includes also redirection, this  could interrupt the duplication process .

What happen is this: when you create a new site as a copy of another, depending on the settings, MultilingualPress will activate all the plugins of the source site also in the new one.

But if any of these plugins perform a redirection within the activation, this would lead to a process interruption. The redirection will stop the duplication process.

## The solution: uncheck plugin activation option

How to solve this? Luckily MultilingualPress has another option that prevent this issue to happen right before to start the creation process.

You just need to **uncheck the "_Activate all plugins that are active on the source site_"** as reported in the picture here below.

[caption id="attachment_14403" align="aligncenter" width="2336"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2020/11/Create-a-new-site-preventing-site-activation.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2020/11/Create-a-new-site-preventing-site-activation.png) Create a new site preventing redirects on activation[/caption]

This way MultilingualPress duplicates the source site, but it also does not activate all the plugin in the remote site during the process.

So no redirection happens, and the duplication completes properly.

Of course, after the creation, all the needed plugin need to be manually activated.