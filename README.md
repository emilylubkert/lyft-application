# Technical Sample
## Lyft Software Engineering Apprenticeship application

### Description
This is a simple web application that accepts a POST request to the route "/test" with one argument "string_to_cut". This request returns a JSON object with the key “return_string” and a string containing every third letter from the original string.

### How to Run
You can access the deployed app here: https://get-every-third.herokuapp.com/ (coming soon!)

To run locally:
- Clone this repo `git clone https://github.com/emilylubkert/lyft-application`
- `npm install`
- `npm start` to run app
- `npm test` to run unit tests
- run app on http://localhost:8080/

### How to Use
Enter a string into the input box, and press submit to see response.

### API
#### POST /test  
- Parameter: string_to_cut, the string that we want to get every 3rd character from  
- In body: `{"string_to_cut" : "anyStringHere"}`  
- Content-Type: application/json <br/>
- Try out:    
    `curl -X POST https://get-every-third.herokuapp.com/test --data '{"string_to_cut": "iamyourlyftdriver"}' -H 'Content-Type: application/json' ` <br/>
    Expect to see `{"return_string":"muydv"}` <br/>
##### Server methods: 
- If string_to_cut was less than 3 characters, send an error message to the client and return/exit function
- Loop through string_to_cut and get every 3rd character with charAt()
- Add characters to array
- Join array elements into new string
- Send { return_string: "newString" } to client with status code 201

### Contact
elubkert@gmail.com

### License
MIT
