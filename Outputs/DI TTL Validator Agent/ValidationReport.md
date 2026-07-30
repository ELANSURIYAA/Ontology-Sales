{"error":"Conversion incomplete: OWLToTurtleRDFLibConverterTool returned only a truncated Turtle fragment (ontology header) rather than the full TTL serialization of all classes and properties. Please rerun the converter on the complete OWL content and ensure the full graph is serialized.","status":"failure"}

----------

{
  "status": "failure",
  "error": "TTL ontology content is missing or incomplete. The OWLToTurtleRDFLibConverterTool returned only a truncated ontology header and an error: \"Conversion incomplete: OWLToTurtleRDFLibConverterTool returned only a truncated Turtle fragment (ontology header) rather than the full TTL serialization of all classes and properties. Please rerun the converter on the complete OWL content and ensure the full graph is serialized.\" Because the full, valid Turtle content from the DI OWL TO TTL CONVERTER AGENT was not provided, required input 'content' for the GitHub file write operation is not present. The EnterpriseOntology.ttl file was NOT created or updated in ELANSURIYAA/Ontology-Sales. Please rerun the converter to obtain the complete TTL, then call this GitHub writer workflow again with the full ontology content."
}

----------

{
  "status": "failure",
  "error": "Unable to retrieve TTL ontology file from GitHub. The file 'Outputs/DI OWL To TTL Converter Agent /EnterpriseOntology.ttl' in repository 'ELANSURIYAA/Ontology-Sales' on branch 'main' returned: 404 Client Error: Not Found for the requested content URL. This indicates that the file either does not exist at the specified path, the folder or filename is incorrect (note: spaces and exact casing in 'Outputs/DI OWL To TTL Converter Agent ' and 'EnterpriseOntology.ttl' must match the repository), or it has not yet been created due to the earlier OWL-to-TTL conversion failure. Please verify the exact path and filename in the repository, ensure the OWLToTurtle converter is rerun to produce the complete TTL content, commit the resulting 'EnterpriseOntology.ttl' to the correct folder in 'ELANSURIYAA/Ontology-Sales', and then retry this retrieval operation."
}

----------

Failure

Validation could not be completed because one or both ontology inputs are invalid.