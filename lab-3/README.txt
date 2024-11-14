Your goal for this lab is to take your lab-2 solution and modify it to fetch DHIS2 tracked entities using the DHIS2 component.

Instructions:

1. Copy the YAML file containing the routes from the previous lab solution (i.e., lab-2) to this directory (i.e., lab-3).
2. Open the YAML file and remove the "setBody" and "log" processors from the "readPatient" route.
3. Within the same route, add a "toD" DHIS2 endpoint for fetching tracked entities.
    3.1 The baseApiUrl parameter should be set to https://dev.im.dhis2.org/hisp-training-sri-lanka-2024
    3.2 The username parameter should be set to "admin" and the password parameter set to "district"
    3.3 The path parameter should be set to "tracker/trackedEntities/${headers.id}"
4. Run the route and make sure that there are no errors in your terminal.
5. Test the running route by accessing "http://localhost:8080/fhir/Patient/PMwiQgRZlNU" from your browser. You should get back a JSON response containing the requested tracked entity.

Bonus:

    1. Add an operation to the OpenAPI definition "Patient.openapi.yaml" to fetch all patients.
    2. Create a new route for the new operation that fetches all patients from the online HAPI FHIR server https://hapi.fhir.org/baseR4. Remember to read the FHIR component docs: https://camel.apache.org/components/next/fhir-component.html. Hint: the endpoint URI should be "fhir:search/searchByUrl"