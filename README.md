# note-newman-test

note-newman-test is a sample newman test script for note-api

## Example of note-api

[note-api-by-crystal](https://github.com/shiba-hiro/note-api-by-crystal)

## Requirements

1. Install Newman  
https://www.npmjs.com/package/newman

2. Run note-api  
Please refer to the link at [Example of note-api](#example-of-note-api)


## Usage

After note-api server starts up on your local, execute commands;  
```
$ git clone https://github.com/shiba-hiro/note-newman-test
$ cd note-newman-test
$ newman run note-v1-newman-collection.postman_collection.json -e note-api-local.postman_environment.json 
```

Then, you will see the test result like this;  
```
newman

note-v1-newman-collection

→ notes-v1-get-list
  POST http://localhost:3000/v1/notes [201 Created, 317B, 17ms]
  POST http://localhost:3000/v1/notes [201 Created, 317B, 5ms]
  POST http://localhost:3000/v1/notes [201 Created, 317B, 5ms]
  POST http://localhost:3000/v1/notes [201 Created, 317B, 4ms]
  POST http://localhost:3000/v1/notes [201 Created, 317B, 5ms]
  POST http://localhost:3000/v1/notes [201 Created, 317B, 5ms]
  POST http://localhost:3000/v1/notes [201 Created, 317B, 4ms]
  POST http://localhost:3000/v1/notes [201 Created, 317B, 5ms]
  POST http://localhost:3000/v1/notes [201 Created, 317B, 6ms]
  POST http://localhost:3000/v1/notes [201 Created, 317B, 7ms]
  GET http://localhost:3000/v1/notes/ [200 OK, 4.56KB, 4ms]
  ✓  Status code is 200
  ✓  Response contains expected resources
  ✓  Items have expected fields.

→ notes-v1-post
  POST http://localhost:3000/v1/notes/ [201 Created, 317B, 7ms]
  ✓  Status code is 201
  ✓  Item has expected fields.
  ✓  Save-operation is reflected.

→ notes-v1-get
  POST http://localhost:3000/v1/notes [201 Created, 317B, 6ms]
  GET http://localhost:3000/v1/notes/aa08f6fc-f784-4f0a-bc99-37459e7c7e63 [200 OK, 312B, 2ms]
  ✓  Status code is 200
  ✓  Response is expected resource
  ✓  Item has expected fields.

→ notes-v1-put
  POST http://localhost:3000/v1/notes [201 Created, 317B, 7ms]
  PUT http://localhost:3000/v1/notes/66ced135-948c-4d3f-b87a-56a0f3764bdd [200 OK, 355B, 8ms]
  ✓  Status code is 200
  ✓  Response is expected resource
  ✓  Item has expected fields.
  ✓  Save-operation is reflected.

→ notes-v1-delete
  POST http://localhost:3000/v1/notes [201 Created, 317B, 6ms]
  DELETE http://localhost:3000/v1/notes/52bba98d-cb99-44f2-9d78-21e58a0f27c6 [204 No Content, 123B, 8ms]
  ✓  Status code is 204
  ✓  Response body is empty

┌─────────────────────────┬──────────┬──────────┐
│                         │ executed │   failed │
├─────────────────────────┼──────────┼──────────┤
│              iterations │        1 │        0 │
├─────────────────────────┼──────────┼──────────┤
│                requests │       18 │        0 │
├─────────────────────────┼──────────┼──────────┤
│            test-scripts │        5 │        0 │
├─────────────────────────┼──────────┼──────────┤
│      prerequest-scripts │        4 │        0 │
├─────────────────────────┼──────────┼──────────┤
│              assertions │       15 │        0 │
├─────────────────────────┴──────────┴──────────┤
│ total run duration: 338ms                     │
├───────────────────────────────────────────────┤
│ total data received: 7.53KB (approx)          │
├───────────────────────────────────────────────┤
│ average response time: 6ms                    │
└───────────────────────────────────────────────┘
```
