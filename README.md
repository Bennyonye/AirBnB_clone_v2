**HBNB - The Console**

This repository kickstarts a student project aimed at replicating the AirBnB website. It initiates with a backend interface, or console, for managing program data. Users can create, update, and delete objects, alongside handling file storage. With JSON serialization/deserialization, data persists between sessions.

---

**Repository Overview by Project Task**

| Task | Files | Description |
| ---- | ----- | ----------- |
| Authors/README File | [AUTHORS](./AUTHORS) | Lists project authors |
| Pep8 | N/A | All code adheres to pep8 standards |
| Unit Testing | [/tests](./tests) | Modules are unit tested |
| Make BaseModel | [/models/base_model.py](./models/base_model.py) | Defines a parent class for model classes |
| Update BaseModel w/ kwargs | [/models/base_model.py](./models/base_model.py) | Enhances functionality for object recreation from dictionary |
| Create FileStorage class | [/models/engine/file_storage.py](./models/engine/file_storage.py), [/models/__init__.py](./models/__init__.py), [/models/base_model.py](./models/base_model.py) | Manages persistent file storage |
| Console 0.0.1 | [console.py](./console.py) | Adds basic console functionalities |
| Console 0.1 | [console.py](./console.py) | Updates console with CRUD operations |
| Create User class | [console.py](./console.py), [/models/engine/file_storage.py](./models/engine/file_storage.py), [/models/user.py](./models/user.py) | Dynamically implements user class |
| More Classes | [/models/user.py](./models/user.py), [/models/place.py](./models/place.py), [/models/city.py](./models/city.py), [/models/amenity.py](./models/amenity.py), [/models/state.py](./models/state.py), [/models/review.py](./models/review.py) | Dynamically implements additional classes |
| Console 1.0 | [console.py](./console.py), [/models/engine/file_storage.py](./models/engine/file_storage.py) | Updates console and file storage for dynamic class handling |

**General Use**

1. Clone this repository.

2. Locate the "console.py" file in the cloned repository.

3. Run the following command:
```
/AirBnB_clone$ ./console.py
```

4. The prompt `(hbnb)` indicates access to the HBNB console. Various commands are available:

- `create`: Creates an instance based on a given class.
- `destroy`: Deletes an object based on class and UUID.
- `show`: Displays an object based on class and UUID.
- `all`: Shows all objects or objects of a specific class.
- `update`: Modifies object attributes based on class and UUID.
- `quit`: Exits the program.

**Alternative Syntax**

Commands can also be issued with an alternative syntax:

- `all`
- `count`
- `show`
- `destroy`
- `update`

**Examples**

- **Primary Command Syntax:**

1. Creating an object:
```
(hbnb) create BaseModel
```
2. Showing an object:
```
(hbnb) show BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
```
3. Destroying an object:
```
(hbnb) destroy BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
```
4. Updating an object:
```
(hbnb) update BaseModel b405fc64-9724-498f-b405-e4071c3d857f first_name "person"
```

- **Alternative Syntax:**

1. Showing all User objects:
```
(hbnb) User.all()
```
2. Destroying a User:
```
(hbnb) User.destroy("99f45908-1d17-46d1-9dd2-b7571128115b")
```
3. Updating a User (by attribute):
```
(hbnb) User.update("98bea5de-9cb0-4d78-8a9d-c4de03521c30", name "Todd the Toad")
```
4. Updating a User (by dictionary):
```
(hbnb) User.update("98bea5de-9cb0-4d78-8a9d-c4de03521c30", {'name': 'Fred the Frog', 'age': 9})
```
