# New Zealand Research Information System (NZRIS) Application Programming Interface (API) Specification
NZRIS will be a national, online hub of information about research, science and innovation in New Zealand. You can find more about the NZRIS project at https://www.mbie.govt.nz/science-and-technology/science-and-innovation/research-and-data/nzris/. This repository contains part of the full descrition of the NZRIS API which will provide a way for organisations to submit data to NZRIS. The full description is publically available [on the Ministry of Business, Innovation and Employment (MBIE) website](https://www.mbie.govt.nz/science-and-technology/science-and-innovation/research-and-data/nzris/nzris-tools-resources/).

## The data structure of a submission and full API definition are available
Data needs to be submitted to the API in [JavaScript Object Notation (JSON)](https://en.wikipedia.org/wiki/JSON). There is a set structure that is set by the '[Swagger](https://en.wikipedia.org/wiki/Swagger_(software)) definition' which is a script written in [YAML](https://en.wikipedia.org/wiki/YAML) that dictates how the API is to operate. This definition is available in [api-definition.yaml], and viewable with the [Swagger Editor](https://editor.swagger.io/) (see below). The JSON input format comes from this definition and an example created with the [Swagger Editor](https://editor.swagger.io/) based on the definition is available as [submission-example.json].

### The API definition can be viewed using the Swagger Editor
The [Swagger Editor](https://editor.swagger.io/) provides a way to easily veiw Swagger YAML definitions. To view the definition for the NZRIS project:
1. Go to [https://editor.swagger.io/].
2. Copy the text from the [API definition](https://raw.githubusercontent.com/new-zealand-research-information-system/nzris-api-specification/master/api-definition.yaml).
3. Paste the copied text into the left hand side of the Swagger Editor.
