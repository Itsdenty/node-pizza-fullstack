# node-pizza-fullstack
This is the fullstack version of the node pizza app with raw node api and html css and javascript

## Made With
  ### Raw Node Api
    * https module
    * url module 
    * stringdecoder module
    * fs module
    * path module
    * util module
    * debug module

  ### Continuous Integration
    * Travis CI & Codeclimate for test automation
    * Coveralls for test coverage report
  
  ### Test-Driven Development
    * Mocha, Chai and Supertest for api route testing

## Installation.
  * Install [Nodejs](https://nodejs.org/en/download/)
  * Clone this repo ``` git clone https://github.com/itsdenty/andela-vlf-challenge.git ```
  * Run ```node index.js``` to initiate server
  * Modify lib/config.js to provision mailgun api key

## Features covered by the api
* Users canlog in and logout of the app. via the token get and delete endpoints, tokens expires after 24 hours
* Users can be created via the users post endpoint
* Users can check their existing details via the users get endpoint
* Users can be edit their existing details via the users put endpoint
* Users can delete their profile via the users delete endpoint
* Users can check available items via the items get endpoint
* A user can add items to cart via the carts post endpoint 
* A user can modify cart content via the carts put endpoint
* A user can check his current cart content via the carts get endpoint
* A user can empty his cart via the carts delete endpoint
* Drivers can either accept or reject a ride request.

## Available APIs
<table>
  <tr>
      <th>HTTP REQUEST VERB</th>
      <th>API ENDPOINT/PATH</th>
      <th>ACTION</th>
  </tr>
  <tr>
      <td>GET</td>
      <td>/users</td>
      <td>list the users details via a required query paramter {email}</td>
  </tr> 
  <tr>
      <td>POST</td>
      <td>/users</td>
      <td>Create users profile with email, customerName, address and password captured as post parameters</td>
  </tr>
  <tr>
    <td>PUT</td>
    <td>/users</td>
    <td>Edit user's details query parameters {email}</td>
  </tr>
  <tr>
      <td>DELETE</td>
      <td>/users</td>
      <td>Delete user's data query parameter {email}</td>
  </tr>
  <tr>
    <td>GET</td>
    <td>/items</td>
    <td>Get the items available on the pizza menu</td>
  </tr>
  <tr>
      <td>POST</td>
      <td>/carts</td>
      <td>Allows users to add pizza to their cart parameter is an array of pizza items with referenced item id and quantity to order</td>
  </tr>
  <tr>
      <td>GET</td>
      <td>/carts</td>
      <td>Gets the current cart details</td>
  </tr>
  <tr>
      <td>PUT</td>
      <td>/carts</td>
      <td>modify items present in your active cart</td>
  </tr>
  <tr>
      <td>DELETE</td>
      <td>/carts</td>
      <td>Empty the content of your current cart</td>
  </tr>
  <tr>
      <td>GET</td>
      <td>/order</td>
      <td>
      Process the cart content, charge the user and send them their order receipt</td>
  </tr>
</table>

## License and Copyright
&copy; Abd-afeez Abd-hamid

Licensed under the [MIT License](LICENSE).