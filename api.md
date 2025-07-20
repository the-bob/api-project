## API (HTTP Methods)


[back](./README.md)

<hr/> 

* `POST` - This method is used for Reserving a class.
* `PUT` - This method is used for Updating a Reservation.
* `GET` - This method is for Read Operations.

## API JSON Structure

*NOTE:* `<VERSION>`: this will be a major version format i.e. `v1`


### Reading the Venue Data
  
  * Endpoint: `/rest/<VERSION>/{venueid}`
  * Method: `GET`
  * Response:
    ```json
    [
        {
            "id": string,
            "name": string,
            "address": string,
            "email": string, 
            "class_size_limit": number,
            "classes": [
                {
                    "classid": string,
                    "name": string,
                    "date": string,
                    "class_size_limit": number
                },
            ]
        },
    ]
    ```

### Reserving Classes

  * Endpoint: `/rest/<VERSION>/reserve`
  * Method: `POST`
  * Request:
    ```json
    {
        "classid": string,
        "userid": string, 
    }
    ```

  * Response:
    ```json
    {
        "classid": string,
        "name": string,
        "date": string,
        "class_size_limit": number,
        "status": string,
        "class_reservationid": string,
    }
    ```

### Cancelling a Reservation:
*NOTE:* Assumption here is we won't delete any records (for historical purposes), but if needs be, then we can set the method to `DELETE`.
  
  * Endpoint: `/rest/<VERSION>/reserve/{class_reservationid}`
  * Method: `PUT`
  * Request:
    ```json
    {
        "classid": string,
        "userid": string
    }
    ```
<hr/> 

[back](./README.md)