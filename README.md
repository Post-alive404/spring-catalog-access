# Spring Catalog Access

There are three roles:
- MANAGER
- EMPLOYEE
- CUSTOMER

There are three controller and related paths:
- [EmployeesController](src/main/java/com/epam/rd/autotasks/catalogaccess/EmployeesController.java)
    : `/employees`
    - GET requests are available to managers and employees,
    - POST requests are available to managers only,
- [SalaryController](src/main/java/com/epam/rd/autotasks/catalogaccess/SalaryController.java)
  : `/salaries`
    - Request to all salaries (`/salaries`) is available to managers only,
    - Request to the salary of the employee (`/salaries`) is available to any employee or manager,
- [CatalogController](src/main/java/com/epam/rd/autotasks/catalogaccess/CatalogController.java)
  : `/catalog`
    - Requests to catalog are available to any manager, employee or customer.

Spring Security in [WebSecurityConfig](src/main/java/com/epam/rd/autotasks/catalogaccess/WebSecurityConfig.java).\
