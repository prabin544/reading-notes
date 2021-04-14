# Web API design
Most modern web applications expose APIs that clients can use to interact with the application. A well-designed web API should aim to support:

Platform independence. Any client should be able to call the API, regardless of how the API is implemented internally. This requires using standard protocols, and having a mechanism whereby the client and the web service can agree on the format of the data to exchange.

Service evolution. The web API should be able to evolve and add functionality independently from client applications. As the API evolves, existing client applications should continue to function without modification. All functionality should be discoverable so that client applications can fully use it.

This guidance describes issues that you should consider when designing a web API.

# Best practices for REST API design  
- Accept and respond with JSON
- Use nouns instead of verbs in endpoint paths  
- Name collections with plural nouns  
  We should name collections with plural nouns. It’s not often that we only want to get a single item, so we should be consistent with our naming, we should use plural nouns.
  We use plurals to be consistent with what’s in our databases. Tables usually have more than one entry and are named to reflect that, so to be consistent with them, we should use the same language as the table the API accesses. 
  With the /articles endpoint, we have the plural form for all endpoints, so we don’t have to change it to be plural.  
- Nesting resources for hierarchical objects  
- Handle errors gracefully and return standard error codes

# Define operations in terms of HTTP methods  
- GET retrieves a representation of the resource at the specified URI. The body of the response message contains the details of the requested resource.
- POST creates a new resource at the specified URI. The body of the request message provides the details of the new resource. Note that POST can also be used to trigger operations that don't actually create resources.
- PUT either creates or replaces the resource at the specified URI. The body of the request message specifies the resource to be created or updated.
- PATCH performs a partial update of a resource. The request body specifies the set of changes to apply to the resource.
- DELETE removes the resource at the specified URI.

[Source](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)
