# Interfaces description
## Campaign Manager
Required and provided interfaces for the Campaign Manager component.

![interfaces.png](/.attachments/interfaces-86aa047d-46de-4b50-b8c0-8e9b5aa91911.png)

The following sections list the provided interfaces.
### /annotation
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