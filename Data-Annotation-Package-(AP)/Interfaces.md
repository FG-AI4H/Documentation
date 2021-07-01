# Interfaces description
Interfaces are decribed using OpenAPI 3.0 specifications. 

The Swagger can be found here
https://app.swaggerhub.com/apis/mllabai/FG-AI4H-OC-AP/0.0.1#/

## Campaign Manager
Required and provided interfaces for the Campaign Manager component.

![interfaces.png](/.attachments/interfaces-e7d30639-b9f8-428b-ba32-fac992f14bdc.png)

The following sections list the provided interfaces.

### /tasks
#### get
This operation gets the next available annotation task that needs to be processed.

```
/tasks:
    get:
      summary: Gets next annotation task
      description: >-
        This operation gets the next available annotation task that needs to be processed.
      parameters:
      - in: query
        name: campaignId
        schema:
          type: integer
        required: true
        description: Numeric ID of the annotation campaign to use
      responses:
        '200':
          description: An AnnotationTask object
          content:
              application/json:
                schema:
                  type: object
                  properties:
                    annotationTaskId:
                      type: string
                      format: uuid
                      description: The annotation task ID.
                    fileUrl:
                      type: string
                      description: The URL of the image to annotate.
```

### /annotations
#### post
This operation creates an annotation for an annotation task. The annotation is represented as a nifti file.
```
/annotations:
    post:
      summary: Creates an annotation
      description: >-
        This operation creates an annotation for an annotation task. The annotation is represented as a nifti file.
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