Starting from MultilingualPress version 4, assigning a language to a subsite through WP-CLI is possible. Open your shell and go to the WordPress directory where the MultlingualPress plugin is installed and activated.

From there, if you want to assign to the sub-site with id 41, the Spanish language, for example, you can use the following command:

wp mlp setLanguage --site-id=4 --language='es-ES'

For further information, you can use the following online help:

wp mlp setLanguage help