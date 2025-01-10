If you want to connect content programmatically across sites you need to know the IDs of the posts you want to connect beforehand. So let say that we have 3 sites with site ids 1, 2 and 3 and we want to connect a post with the following post ids on each site:

post id 42 in site 1  
post id 123 in site 2  
post id 321 in site 3

Following code snippet creates the `$contentIds` array of key value pairs with site id as key and post id as value. Afterwards we pass it to the `createRelationship` method as first parameter to connect the content.

$api = \Inpsyde\MultilingualPress\resolve(
\Inpsyde\MultilingualPress\Framework\Api\ContentRelations::class
);

$contentIds = [
1 => 42,
2 => 123,
3 => 321,
];

$api->createRelationship($contentIds, 'post');

In the example above, the context is set to "post", which represents the relationship for posts or custom post types. However, you can also use "term" as the context for creating relationships between taxonomy terms like categories or tags, and "comment" for connecting comments across translations.