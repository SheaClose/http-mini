## Joe's Auto API Docs:

  - Base url: https://joes-autos.herokuapp.com

### *Vehicles*


#### GET

##### Get all vehicles
- Request url: base url + '/api/vehicles'
- Response: All vehicles

##### Get vehicles by color
- Request url: base url + '/api/vehicles'
- Send with query: i.e. `?color=red`
- Response: All vehicles that match given color

##### Get vehicles newer than specified year
- Request url: base url + '/api/vehicles'
- Send with query: i.e. `?year=1998`
- Response: All vehicles newer than given year

##### Get vehicles by make
- Request url: base url + '/api/vehicles'
- Send with query: i.e. `?make=ford`
- Response: All vehicles that match given car make

#### POST

##### Add vehicle
- Request url: base url + '/api/vehicles'
- Need make, model, year, color, price in body of request. ID is auto-generated.
- Response: updated vehicles array.

#### PUT

##### Increase/decrease price of car by $1000
- Request url: base url + '/api/vehicle/:id/:change'
  - `id` is the id of the vehicle
  - Value of `change` needs to be either `up` or `down`.
- Response: updated vehicles array

#### DELETE

##### Delete vehicle by id
- Request url: base url + '/api/vehicles/:id'
- Response: updated vehicles array


### *Potential Buyers*

#### GET

##### Get all buyers
- Request url: base url + '/api/buyers'
- Response: array of all buyers

##### Get buyers by name/letters
- Request url: base url + '/api/buyers'
  - Send with query: i.e. `?name=Lindsey`
  - Will find names that match letters sent
- Response: Array of buyers with matching names

#### POST

##### Add potential buyer
- Request url: base url + '/api/buyers'
  - Need name, phone, address in body of request. ID is auto-generated.
- Response: updated buyers array

#### DELETE

##### Delete buyer by id
- Request url: base url + '/api/buyers/:id'
  - `id` param is the id of the buyer getting removed
- Response: updated buyers array
