# Backend 💾
 
API created for the connection to the SQL database, developed in pyhton.

## Start 🚀 
1) IotDB.sql to create the data base.
2) IotPA.sql for stored procedures.
3) inputEjemplos.sql to fill data base.

To get information from the API, a GET request must be made to any of the available routes with their respective parameters:

## API 🌐 
### Adminstrator / Users
```
/login?username=&contrasena=
/insert?name=&email=&username=&password=&date_register=&admin=
/delete?username= 
/modify?username=&name=&email=&status=
/search?username=
/showAllUser
```
### Spaces
#### Stage
```
 /insertStage?id_stage=&name=&user=&admin=
 /deleteStage?id_stage= 
 /searchStage?id_stage=
 /modifyStage?id_stage=&name=
 /showAllStage
```
#### Floor
```
 /insertFloor?id_floor=&name=&id_stage=
 /deleteFloor?id_floor= 
 /searchFloor?id_floor=
 /modify?id_floor=&name=
 /showAllFloor
```
#### Room
```
 /insertRoom?id_room=&name=&id_floor=&id_scenario=
 /deleteRoom?id_room= 
 /searchRoom?id_room=
 /modify?id_room=&name=&id_scenario=
 /showAllRoom
```

### Devices
```
 /insertProduct?id_product=&name=&description=&os=&id_device=&status=&brand=&model=&x=&y=&id_room=
 /insertSensor?id_sensor=&type=&firmware=&clasification=&id_device=&status=&brand=&model=&x=&y=&id_room=
 /deleteDevice?id_device=
 /searchDevice?id_device=
 /type?type_device=
 /modifyDevice?id_device=&brand=&model=&x=&y=
 /showAllDevice
```

It returns a flask.Response() and a status code 200. This can be converted to a JSON with JSON.parse(); the structure of the response depends on the parameters that are given.

⚠️In the login part, a password encryption key is "asdfghjkl", while the encryption method is salt.
