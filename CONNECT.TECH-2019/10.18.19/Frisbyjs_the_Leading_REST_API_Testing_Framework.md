# Frisby.js: The Leading REST API Testing Framework
> Vance Lucas

## Why test your API?
- because it is a contract, even if not publicly released!

## Why Frisby.js?
- specifically built for REST API's

## Frisby.js: The Early Years
- First started in 2011 while working on the Bible app
	- migrating from V1->V2 (new language, switch to Google cloud)

### Solution: requirements
- integration tests for the API
- must be automated
- must integrate with CI build
- must be able to test JSON structure, keys, types
- Must be able to test response status, body, etc
- Tests for error response
- Custom assertions
- Support for auth, cookies, custom headers


## Frisby V2
- Fully embracing Jest/Jasmine (async)
- Fully promise-based (based on 'fetch')
- jest is test runner
- smaller API surface

