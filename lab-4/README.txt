This lab will complete the circle in creating a FHIR gateway for DHIS2.

Instructions:

1. Copy the YAML file containing the routes from the previous lab solution (i.e., lab-3) to this directory (i.e., lab-4).
2. Add the following processor to the "readPatient" route which transforms the output of the DHIS2 endpoint:

    - transform:
        datasonnet:
          expression: resource:file:patient.json.ds
          resultType: java.lang.String
          bodyMediaType: application/json
          outputMediaType: application/json

3. Run the route and make sure that there are no errors in your terminal.
4. Test the running route by accessing "http://localhost:8080/fhir/Patient/PMwiQgRZlNU" from your browser. You should get back a FHIR response like this:

{
  "resourceType": "Patient",
  "id": "PMwiQgRZlNU",
  "name": [
    {
      "family": "Abraham"
    }
  ]
}

5. Modify the DataSonnet script "patient.json.ds" so that the response is as follows (DO NOT hard-code the given name in the DataSonnet script):

{
  "resourceType": "Patient",
  "id": "PMwiQgRZlNU",
  "name": [
    {
      "family": "Abraham"
    },
    {
      "given": [
        "Haddas"
      ]
    }
  ]
}
