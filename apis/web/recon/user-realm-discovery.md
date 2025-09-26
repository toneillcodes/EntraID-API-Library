# User Realm Discovery Endpoint

## Description

## Usage and Examples
A GET request to the ```getuserrealm.srf``` endpoint with the target domain will respond with JSON
```
https://login.microsoftonline.com/getuserrealm.srf?login=$domain
```

Example Request  
``` 
https://login.microsoftonline.com/getuserrealm.srf?login=example.com
```

Example Response
```
{"State":4,"UserState":1,"Login":"example.com","NameSpaceType":"Managed","DomainName":"example.com","FederationBrandName":"Example Corp","CloudInstanceName":"microsoftonline.com","CloudInstanceIssuerUri":"urn:federation:MicrosoftOnline"}
```

Switch to enable XML-formatted response
```
https://login.microsoftonline.com/getuserrealm.srf?login=$domain&xml=1
```

Example XML Response
```
<RealmInfo Success="true"><State>4</State><UserState>1</UserState><Login>example.com</Login><NameSpaceType>Managed</NameSpaceType><DomainName>example.com</DomainName><IsFederatedNS>false</IsFederatedNS><FederationBrandName>Example Corp</FederationBrandName><CloudInstanceName>microsoftonline.com</CloudInstanceName><CloudInstanceIssuerUri>urn:federation:MicrosoftOnline</CloudInstanceIssuerUri></RealmInfo>
```
