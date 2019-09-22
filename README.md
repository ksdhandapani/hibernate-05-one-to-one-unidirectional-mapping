# hibernate-05-one-to-one-unidirectional-mapping
One To One Unidirectional Example
In this example we have below entity classes
- **Employee**
- **Address**
- In Employee class employee_id is a primary key
- In Address class address_id is a primary key
- In employee class address_id is a forieign key

Postman sample request and response
- **Method :** POST
- **URL :** http://localhost:8080/hibernate-05-one-to-one-mapping/api/employee
- **Request Body :**
```
{
	"employeeId": 0,
	"employeeName":"Chandru R",
	"department":"Development",
	"gender": "Male",
	"address": {
		"streetName":"Sankara Madam Street",
		"city":"Emakandanur",
		"state": "Tamil Nadu",
		"country": "India"
	}
}
```
- **Response Body :**
```
{
    "data": {
        "employeeId": 1,
        "employeeName": "Chandru R",
        "gender": "Male",
        "department": "Development",
        "address": {
            "addressId": 1,
            "streetName": "Sankara Madam Street",
            "city": "Emakandanur",
            "state": "Tamil Nadu",
            "country": "India"
        }
    },
    "message": "Employee saved successfully",
    "exception": false,
    "success": true
}
```
