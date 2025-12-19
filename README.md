# Employee Management System (OOP Project)

This project manages different types of employees (**Managers** and **Developers**) within a department structure. By leveraging **Object-Oriented Programming (OOP)** principles, the code is modular, allowing for easy updates and the addition of new employee roles.

---

## OOP Principles Implemented

### 1. Encapsulation
- Sensitive data like employee salaries is protected using the `_salary` variable (single underscore).  
- Access to salary is provided through the public method `get_salary()`.

### 2. Inheritance
- **Parent Class:** `Employee` (shared attributes: `name`, `employee_id`, `salary`)  
- **Child Classes:** `Manager` and `Developer` inherit from `Employee` and include role-specific attributes:  
  - Manager: `department`  
  - Developer: `prog_language`

### 3. Polymorphism
- Methods behave differently based on the object type:  
  - `calculate_bonus()` is overridden in child classes:  
    - Standard Employee: 5% bonus  
    - Developer: 10% bonus  
    - Manager: 15% bonus  
  - `display_info()` prints role-specific details along with standard employee data

### 4. Abstraction
- Complex operations are hidden from the user:  
  - `Department.add_employee()` allows adding employees without exposing underlying list management.

---

## Usage Example

```python
# Create employee objects
dev1 = Developer("Lucy", "D001", 6000, "Python")
manager1 = Manager("Justine", "M001", 10000, "Engineering")

# Create a department and add employees
engineering_dept = Department("Engineering")
engineering_dept.add_employee(dev1)
engineering_dept.add_employee(manager1)

# Display department staff
engineering_dept.display_employees()


## Features

Role-Specific Data: Tracks unique information for different job types
Department Management: Aggregates employees into organizational units
Dynamic Calculations: Automatically calculates bonuses based on employee roles


This project was developed to practice and showcase fundamental skills in Object-Oriented Programming and Python application design, demonstrating encapsulation, inheritance, polymorphism, and abstraction in a practical scenario.
