# Json-Parser
The Parser is able to validate all JSON strings raise the error accordingly. It gives an error message in case of invalid JSON and along with it.

## Pitfalls
* Validation of duplicate key is not implemented.

## Inside Description
The parser takes a json file as input which contains the JSON Object for validating file only. We use Recursive Descent parsing, by creating my own grammer for JSON.

## JSON Grammer
* S -> {X}
* X -> K:Xb	
* K -> "String"
* Xb -> VY | [A]Y
* V -> "String" | NULL | True | False | S 
* Y -> ,X | $
* A -> V Ab 
* Ab -> ,A | $
