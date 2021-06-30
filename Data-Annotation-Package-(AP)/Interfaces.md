# Interfaces description
Interfaces are decribed using OpenAPI 3.0 specifications. 

The Swagger can be found here
https://app.swaggerhub.com/apis/mllabai/FG-AI4H-OC-AP/0.0.1#/

## Campaign Manager
Required and provided interfaces for the Campaign Manager component.

![interfaces.png](/.attachments/interfaces-0ba454b2-bdf6-44d6-ae16-9cdb1331bb65.png)

The following sections list the provided interfaces.

### /annotations
#### post
This operation creates an annotation for an annotation task. The annotation is represented as a nifti file.
```
requestBody:
  content:
     multipart/form-data:
       schema:
         type: object
         properties:
           annotationTaskId:
             type: string
             format: uuid
           niftiFile:
             type: string
             format: binary
 responses: 
   '201':
       description: Created
```