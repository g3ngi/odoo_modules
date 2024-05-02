
# Real Estate Advertising (How to create custom odoo module)
A simple note to create custom odoo module for developers
## Development Environment Setup
There are many  ways to setup the odoo environment, I reccomend these two ways
- [Using docker container](https://github.com/g3ngi/sysadmin-note/tree/main/deployment/install_odoo_docker)
- [Using local odoo server](https://www.odoo.com/documentation/17.0/developer/tutorials/setup_guide.html)



## Module Architecture
Odoo module use MVC architecture  where it has three main components:
- **Model**: handles the data logic, interacts with database 
- **View**: handles data presentation
- **Controller**: handles requests flow, never handle data logic 


### Module Composition
The `MVC` architecture will be implemeted into 4 elements:

a. **Business objects**: Business objects defined as python class and the fields defined is automatically mapped to database columns

b. **Object views**: Define UI display

c. **Data files**: XML or CSV files declaring the model data:

- views or report
- configuration data (module parameterizarion, security rules)
- demonstration data 

d. **Web controllers**: handle requests from web browser

e. **Static web data**: images, CSS or JS used by web interface / website



### Folder Structure
This is the basic folder structure in odoo module

    module_name/
    ├── __init__.py
    ├── __manifest__.py
    ├── models/
    │   ├── __init__.py
    │   └── your_model.py
    ├── views/
    │   ├── __init__.py
    │   └── your_model_views.xml
    └── controllers/
        ├── __init__.py
        └── your_controller.py

