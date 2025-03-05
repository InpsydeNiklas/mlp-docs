# Translating Comments & Product Reviews

**MultilingualPress Comments Support** extends the core functionality of the plugin to manage and synchronize comments (including WooCommerce reviews) across connected multilingual sites. This integration leverages the same principles used for translating posts, pages, and other content types, ensuring that user interactions like comments remain consistent and accessible in multiple languages.

### Key Concepts of Comments Integration

1. **Language Connections for Comments**:  
    Just as MultilingualPress links posts and pages across different language sites, it also connects comments made on content. When two posts (e.g., "First Post English Site" and its Italian counterpart) are linked, their associated comments can be related as translations or copies. This ensures that if a visitor leaves a comment on one language version, that interaction can be propagated or linked to the corresponding version in another language.

2. **Comment Translation Metabox**:  
    In the WordPress admin, when editing a comment on a source site, a **translation metabox** appears below the comment if the Comments module is active. This metabox is similar to those found on posts:
    
    - It allows administrators to **create** a corresponding comment on a connected site in another language.
    - It supports **linking** an existing comment from another site to the current comment.
    - It includes options to **overwrite specific fields**, such as the author information or content, ensuring that translated comments maintain consistency with the source.

3. **Bulk Comment Operations**:  
    MultilingualPress provides features for **bulk copying comments** from one site to another. Through the settings panel of a subsite, administrators can:
    
    - Copy all comments from a source site to a target site for linked content.
    - Enable automatic creation of comments on connected sites whenever a new comment is added to the source site.
    
    These capabilities streamline large-scale comment synchronization, reducing manual effort and ensuring consistency across languages.
    
4. **Integration with Site Creation**:  
    When creating a new site based on an existing one, MultilingualPress can copy over not just posts and pages but also their associated comments. This means that a newly created language site can inherit the conversational history (comments) of the source site, providing context and continuity across translations from the outset.
    

5. **WooCommerce Reviews Support**:  
    The integration is not limited to standard WordPress comments. MultilingualPress extends similar functionality to **WooCommerce product reviews**:
    
    - When products are translated across sites, their reviews can also be linked or replicated.
    - The translation metabox for reviews offers options to copy review content, ratings, and other metadata to corresponding products on other language sites.
    - Bulk settings allow administrators to manage the synchronization of reviews similarly to standard comments.

### Benefits of Comments Integration

- **Consistent User Experience**: Visitors can see and engage with comments on translated content, fostering community interaction across languages.
- **Centralized Management**: Administrators can manage comments for multiple language sites from a single interface, linking, copying, or synchronizing them as needed.
- **SEO and Engagement**: By linking comments across languages, user-generated content becomes richer and more accessible in different regions, improving engagement and potentially contributing to localized SEO efforts.
- **Scalability**: For large, multilingual networks, automated comment linking and bulk operations save time and ensure consistency, essential for enterprise-level setups.

### How It Works Under the Hood

MultilingualPress uses the same relational framework to manage comments as it does for other content types. This involves:

- **Database Relationships**: Establishing links between comment entries on different sites when their parent posts/pages are connected.
- **User Interface Enhancements**: Adding translation metaboxes in the comment editing screen to facilitate manual linking or copying.
- **Module-Based Features**: Activation of the Comments module enables these features, integrating seamlessly with existing WordPress comment handling.

### Next Steps and Further Reading

While this explanation provides an overview of how MultilingualPress handles comments, detailed, step-by-step instructions for activating and using these features are available in specific **How-To** guides. For example, separate documentation might cover:

- How to manually link individual comments between sites.
- How to perform bulk copy operations for comments.
- How to configure WooCommerce reviews synchronization.

For more in-depth guidance, consult the relevant tutorials in the **How-To Guides** section of the MultilingualPress documentation.