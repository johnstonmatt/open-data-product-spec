# Data Pipeline


Data Pipeline is a process whereby a data product pipeline deployment method is defined. Usually the deployment script contains the logic of the individual steps as well as the code chaining the steps together.

Data Pipeline Object's purpose is enabling building, deploying, and running the data product’s code, and storing and giving access to data and metadata. This priciple has been adopted from Data Mesh.

> Example of Data Pipeline component usage:

```javascript
  
"dataPipeline": {
  "infrastructure": {
    "composer": "helm",
    "format": "yaml",
    "status": "development",
    "scriptURL": "http://192.168.10.1/test/runDataPipeline.yml",
    "deploymentDocumentationURL": "http://192.168.10.1/test/docs/DocsDataPipeline.html"
  }, 
  "dataAccess" {
    "type": "API",
    "specification": "OAS",
    "format": "JSON",
    "specURL": "https://swagger.com/petstore.json",
    "dataAccessDocumentationURL": "http://192.168.10.1/test/docs/dataaccessguide.html"
  }
}

  
```
| <div style="width:150px">Element name</div>   | Type  | Options  | Description  |
|---|---|---|---|
| dataPipeline | element | - | Data Pipeline is a process whereby a data product pipeline deployment method is defined |
| composer | string | Any | A name of the package manager, composer or tool |
| format | string  | Any |  Type of script language|
| status | string  | Options for unit are: announcement, draft, development, testing, acceptance, production, sunset, retired |
| scriptURL | URL | Valid URL  | 	The URL of the deployment script. |
| deploymentDocumentationURL | URL | Valid URL  | 	The URL of the deployment documentation |
| DataAccess | element | - | Reference to the ability to use data |
| type | string | Any  | 	Type of data access |
| specification | string | Any  | Type of the data access specification |
| format | string | Any  | 	File format |
| specsURL | URL | Valid URL  | 	The URL of the specification |
| dataAccessDocumentationURL | URL | Valid URL  | The URL of the data access documentation |

