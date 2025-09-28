# Microsoft API Fundamentals

## RESTful APIs
A RESTful API is a reference to an Application Programming Interface that adheres to the Representational State Transfer concepts.  
The APIs provide a way to interact with data or service functionality as a resource that can be accessed or manipulated through standard HTTP methods.

- **Resources and URIs:** Everything is a **resource** (e.g., a user, an function app, a key vault). Each resource is uniquely identified by a **Uniform Resource Identifier (URI)**.
- **Standard Methods:** Operations on these resources are performed using standard **HTTP methods**, which map to common data operations (CRUD):
    - **POST:** Create a new resource. (Create)
    - **GET:** Retrieve a resource. (Read)
    - **PUT/PATCH:** Update an existing resource. (Update)
    - **DELETE:** Remove a resource. (Delete)
- **Statelessness:** The server does not store any client context between requests. Every request from the client must contain all the information the server needs to process it.

## Microsoft Graph vs Azure Resource Manager
Microsoft Graph is a reference to a unified set of APIs to integrate services within the Azure ecosystem.  
"Microsoft Graph is a RESTful web API that enables you to access Microsoft Cloud service resources"  
Source: [Use the Microsoft Graph API](https://learn.microsoft.com/en-us/graph/use-the-api)

Azure Resource Manager aka ARM, is the deployment and management layer for Azure resources.  
Azure Resource Graph aka ARG, is a query service layer that sits on top of ARM.  
"Azure Resource Manager enables you to deploy and manage the infrastructure for your Azure solutions. You organize related resources in resource groups, and deploy your resources with JSON templates."  
Source: [Azure Resource Manager](https://learn.microsoft.com/en-us/rest/api/resources/)

## Concepts
- **REST APIs**: A REST API is an application programming interface (API) that follows the design principles of the REST architectural style. REST is short for representational state transfer, and is a set of rules and guidelines about how you should build a web API.
- **OData Namespace**: The Microsoft Graph API defines most of its resources, methods, and enumerations in the OData namespace, microsoft.graph, in the Microsoft Graph metadata. 
- **Tokens**: Tokens provide access to specific resources, which is defined by the 'scope' of the token.

