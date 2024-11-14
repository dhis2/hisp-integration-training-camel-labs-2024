In this lab, we will edit the previous lab solution to stand up a simple contract-first FHIR API. This OpenAPI spec defining the contract is already present in your lab directory and it is named "Patient.openapi.yaml".

Instructions:

1. Open "Patient.openapi.yaml" and comprehend the API contract.
2. Copy the YAML file from the previous lab solution (i.e., lab-1) to this directory (i.e., lab-2).
3. Open the YAML file containing the route and modify the route such that the "from" URI is set to "direct:readPatient" instead of "timer:yaml". Remove the endpoint parameters since they are not applicable anymore.
4. Within the same YAML file, add a contract-first route in REST DSL that references "Patient.openapi.yaml".
5. Run the route and make sure that there are no errors in your terminal.
6. Test the running route by accessing "http://localhost:8080/fhir/Patient/1234" from your browser. You should get back "Hello Camel from route1".

Bonus: Within the route, log the patient ID from the URL path instead of the route ID. Following this change, you should see printed from your terminal, for example, "Hello Camel from 1234" instead of "Hello Camel from route1".