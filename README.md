# Markdown-Swagger

**register_driver**
----
  Cadastra um motorista.

* **URL**

  /api/v1.0/drivers

* **Method:**

  `POST`
  
* **URL Params**

    **Required:**

    None
   
    **Optional:**
    
    None

* **Data Params**

  * **Data Object:** 
  ```
  {
    "cnh_type_id" : 1,
    "date_of_birth": "1998-12-14 00:00:00",
    "gender_id": 1,
    "last_name": "Bonetti",
    "name": "Leo",
    "own_vehicle": false
  }
  ```

* **Success Response:**

  * **Code:** 201 CREATED <br />
  
    **Content:** 
    ```
    {
    "driver": {
        "cnh_type_id": 4,
        "date_of_birth": "1998-04-05 00:00:00",
        "gender_id": 3,
        "id": 1,
        "last_name": "Pereira Silva",
        "name": "rapha",
        "own_vehicle": false
      },
      "return_message": "Driver Updated"
    }
    ```
 
* **Error Response:**

  * **Code:** 400 BAD REQUEST <br />
  
    **Content:** 
    ```
    {
      "errors_field": {
        
      },
      "return_message": "There is some erros in your request see errors_field"
    }
    ```
    
  * **Code:** 400 BAD REQUEST <br />
   
    **Content:** 
    ```
    {
      "return_message": "JSON Object not found"
    }
    ```

* **Sample Call:**

  ```javascript
  $.ajax({
      url: "localhost/api/v1.0/drivers",
      dataType: "json",
      type : "POST",
      data: JSON.stringify(data),
      success : function(r) {
        console.log(r);
      }
  });
  ```
  
