

## DocumentsCorePack Connector
DocumentsCorePack is a fast & intuitive document generation solution based on Microsoft Dynamics 365 data.
Using MS Word templates, DocumentsCorePack provides you with a set of tools to create and process documents effectively. 

From a document generation wizard that guides users through the process to full document automation - DocumentsCorePack will make your business documents look professional
and help you to process them efficiently!

The DocumentsCorePack Connector brings this functionality to Power Automate and Flows.
[Details](https://www.mscrm-addons.com/Products/DocumentsCorePack) 

## Publisher: PTM EDV Systeme GmbH - mscrm-addons.com Corp.


## Prerequisites

You need to have a Dynamics 365 or Dataverse environment. 

You need to sign up on our website and create a DocumentsCorePack service (14 days free trial available)  [Start here](https://support.mscrm-addons.com/knowledgebase/documentscorepack-online-service-configuration/) 

Get the API Key for your environment:
- [Create a DocumentsCorePack Service](https://www.mscrm-addons.com/Products/DocumentsCorePack/ServiceConfiguration)
- [Optain the API-Key](https://www.mscrm-addons.com/Portals/0/Blog/DCP_CustomConnector_HowTo/c1_obtainAPIKey.PNG)


## API documentation
The API documentation can be found [here](https://support.mscrm-addons.com)


## Supported Operations

### CreateDocument
Creates a new document(pdf,docx,html,..) based on a DocumentsCorePack Template. Optionally it is possible to:
- save to Sharepoint
- print
- attach to an email as attachment
- attach to a record as note

This function is a synchronous function and returns the document and the DocumentJobId.

### CreateDocumentJobAsync
Creates a new DocumentJob (pdf,docx,html,..) based on a DocumentsCorePack Template. Optionally it is possible to 
- save to Sharepoint
- print
- attach to an email as attachment
- attach to a record as note

This function is an async function and does NOT wait for a result. 
It returns a DocumentJobId and you can use the DocumentJobStatus to get the actual status of the job and the DocumentJobResult will return the document.

### CreateDocumentXmlBased
Creates a new document based on our multipart xml schema. Details can be found [here](https://support.mscrm-addons.com/knowledgebase/how-to-build-a-multipartxml-flow-that-concatenates-all-documents-into-one-file/)
The function returns the document and the DocumentJobId.

### CreateDocumentJobXmlBasedAsync
Creates a new DocumentJob based on our multpart xml schema. Details can be found [here](https://support.mscrm-addons.com/knowledgebase/how-to-build-a-multipartxml-flow-that-concatenates-all-documents-into-one-file/)
Attention! The function is asnyc and does NOT wait for a result.
It returns a DocumentJobId and you can use the DocumentJobStatus to get the actual status of the job and the DocumentJobResult will return the document.

### CreateSharepointFolder
Creates Sharepointfolder(s) for an entity following documentlocation rules and waits for the result.
 
### DocumentJobResult
Retrieves a DocumentJobs status information. The result will include the result document, if the job is finished.

### DocumentJobStatus
Retrieves the status of a DocumentJob. Dynamics 365 state/statuscode rules apply.

### PrintDocumentJob
Print the document contentgenerated by a DocumentJob. Attention! The documentjob must already be finished. You can check the state with the function DocumentJobStatus

### PrintFile
Prints a document contentor base64 encoded file. Supported file-formats are PDF and DOCX.

### RunOneClickActionSync
Runs a OneClickAction and waits for the result. 

### RunOneClickActionAsync
Runs a OneClickAction. Attention! The function does NOT wait for a result.

### SendEmail
Send the specified email. 

### SignDocumentJob
This function digitally signs a document job and waits for the result.

### WhoAmI
Returns information about the currently used API Key and associated Service. 

### AttachDocumentJobToEmail
Attach the document contentgenerated by a DocumentJob as attachment to a Dynamics 365 email.

### AttachDocumentJobToNote
Attach the document contentgenerated by a DocumentJob as a note to a Dynamics 365 entity. Attention! The DocumentJob must already be finished. 

### AttachFileToEmail
Attach the document contentor base64 encoded file as attachment to a Dynamics 365 email.

### AttachFileToNote
Attach the document contentor base64 encoded file as a note to a Dynamics 365 entity. Attention! The DocumentJob must already be finished.

### ConcatenateDocumentJobs
Concatenate two document contents (pdf,docx) generated by two DocumentJobs.

### ConcatenateFiles
Concatenates two document contents or base64 encoded file contents (pdf,docx).

### Get Profiles for a UserAPIKey
Returns a list of available environments, each representing a DocumentsCorePack service.

### Get Templates
Returns a list of all available templates for this environment.

### Get DCP Printers
Returns a list of all available DCP Printers for this environment.

### Get OneClickActions
Returns a list of all available OneClickActions for this environment.

### Get SignProviders
Returns a list of all available SignProviders in DocumentsCorePack.

## Obtaining Credentials

First of all, you need to [Create an Account](https://www.mscrm-addons.com/My-Account?returnurl=https%3A%2F%2Fwww.mscrm-addons.com%2FMy-Account) 
and sign up for a DocumentsCorePack Service (14 days free trials available).

Get the API Key for your environment:
- [Create a DocumentsCorePack Service](https://www.mscrm-addons.com/Products/DocumentsCorePack/ServiceConfiguration)
- [Optain the API-Key](https://www.mscrm-addons.com/Portals/0/Blog/DCP_CustomConnector_HowTo/c1_obtainAPIKey.PNG)


If you have question send an email to support@mscrm-addons.com

## Known Issues and Limitations
N/A
