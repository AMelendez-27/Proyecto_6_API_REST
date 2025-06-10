# PROYECTO 6: API REST
## _thePower - Desarrollo Full Stack_

## Description
This has been my first backend development project, developed to meet the criteria required by the training school, in order to obtain the backend developer degree.

## Project Requirements
- Server with Express
- Connection to a MongoDB Atlas database using Mongoose
- Creation of two models
- A seed that uploads data to one of the collections
- A relationship between collections, an array of related data
- Full CRUD for both collections
- README with project documentation, specifying the endpoints and what each one does
- When updating a collection that has an array of related data, we don’t want this data to be deleted
- We will avoid duplicates in the related array

## Tech

Tech stack list for this project
- Node.js
- Express
- Mongoose
- MongoDB
- DotEnv
- Nodemon

## Installation

This project requires [Node.js](https://nodejs.org/) v20.10+ to run.

Install the dependencies and devDependencies and start the server.

```sh
cd [project folder name]
npm i
npm run dev
```

## Endpoints
#### _CARS_

| HTTP Method | Route                     | Description                         | Parameters/Body (Example)               |
|-------------|---------------------------|-----------------------------------|-----------------------------------------|
| `GET`       | `/api/vly/cars`           | Get all cars                      | -                                       |
| `GET`       | `/api/vly/cars/:id`       | Get a car by ID                   | `:id` (e.g., `"507f1f77bcf86cd799439011"`)|
| `POST`      | `/api/vly/cars`           | Create a new car                  | `{ "brand": "Toyota", "model": "Corolla", "type": "Suv", "price":  30000}` |
| `PUT`       | `/api/vly/cars/:id`       | Update a car                     | `:id` + Body (e.g., `{ "model": Mondeo }`)  |
| `DELETE`    | `/api/vly/cars/:id`       | Delete a car                     | `:id` (Car ID)                          |

#### _DEALERSHIPS_
| HTTP Method | Route                        | Description                      | Parameters/Body (Example)               |
|-------------|------------------------------|---------------------------------|-----------------------------------------|
| `GET`       | `/api/vly/carDealerships`    | Get all dealerships             | -                                       |
| `GET`       | `/api/vly/carDealerships/:id`| Get a dealership by ID          | `:id` (e.g., `"658a1f77bcf86cd799439012"`)|
| `POST`      | `/api/vly/carDealerships`    | Create a new dealership          | `{ "name": "AutoMax", "location": "Madrid", "size": 140, "cars": ["507f1f77bcf86cd799439011", "f1fcd79943555adf43256", "df2adf243cd79942adf243cadf256"] }` |
| `PUT`       | `/api/vly/carDealerships/:id`| Update a dealership             | `:id` + Body (e.g., `{ "location": "Barcelona" }`) |
| `DELETE`    | `/api/vly/carDealerships/:id`| Delete a dealership             | `:id` (Dealership ID)                   |


---
---
---