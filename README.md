 <h1 align="center">Employee Management System</h1>

## On Sidebar
- Dashboard
- Employees Management and
- System Management

    <ol>
        <li>Country</li>
        <li>State</li>
        <li>City</li>
        <li>Department</li>
    </ol>

- User Management
    <ol>
        <li>User</li>
    </ol>

## Authentication

- User will be able to login using email and password
- Three (3) failed attempt will lock the user for 5 min

## User Management

- Create, update and delete users
- Change password
- Search users by user name and email

## Employee Management

- List of employees with search and filter by name and department
- Create, update and delete employees


## System Managment
- Country
    <ol>
        <li>List Countries with Search</li>
        <li>Create, update and delete</li>
    </ol>
- State
    <ol>
        <li>List States with Search</li>
        <li>Create, update and delete</li>
    </ol>
- City
    <ol>
        <li>List Cities with Search</li>
        <li>Create, update and delete</li>
    </ol>
- Department
    <ol>
        <li>List departments with Search</li>
        <li>Create, update and delete</li>
    </ol>

## Create API endpoint to list all employees order alphabetically by last name.

<table>
    <tr>
        <th>employees</th>
        <td>id</td>
        <td>integer</td>
        <td></td>
    </tr>
    <tr>
        <th></th>
        <td>first_name</td>
        <td>string</td>
        <td>fillable</td>
    </tr>
    <tr>
        <th></th>
        <td>last_name</td>
        <td>string</td>
        <td>fillable</td>
    </tr>
    <tr>
        <th></th>
        <td>address</td>
        <td>string</td>
        <td>fillable</td>
    </tr>
    <tr>
        <th></th>
        <td>department_id</td>
        <td>foreignId('department_id')->constrained()->cascadeOnDelete()</td>
        <td>fillable</td>
    </tr>
    <tr>
        <th></th>
        <td>city_id</td>
        <td>foreignId('city_id')->constrained()->cascadeOnDelete()</td>
        <td>fillable</td>
    </tr>
    <tr>
        <th></th>
        <td>state_id</td>
        <td>foreignId('state_id')->constrained()->cascadeOnDelete()</td>
        <td>fillable</td>
    </tr>
    <tr>
        <th></th>
        <td>country_id</td>
        <td>foreignId('country_id')->constrained()->cascadeOnDelete()</td>
        <td>fillable</td>
    </tr>
    <tr>
        <th></th>
        <td>zip_code</td>
        <td>char</td>
        <td>fillable</td>
    </tr>
    <tr>
        <th></th>
        <td>birth_date</td>
        <td>date</td>
        <td>fillable</td>
    </tr>
    <tr>
        <th></th>
        <td>date_hired</td>
        <td>date</td>
        <td>fillable</td>
    </tr>
    <tr>
        <th></th>
        <td>timestamp</td>
        <td></td>
        <td></td>
    </tr>
</table>

<table>
    <tr>
        <th>countries</th>
        <td>id</td>
        <td>integer</td>
        <td></td>
    </tr>
    <tr>
        <th></th>
        <td>country_code</td>
        <td>char</td>
        <td>fillable</td>
    </tr>
    <tr>
        <th></th>
        <td>name</td>
        <td>string</td>
        <td>fillable</td>
    </tr>
    <tr>
        <th></th>
        <td>timestamp</td>
        <td></td>
        <td></td>
    </tr>
</table>

<table>
    <tr>
        <th>states</th>
        <td>id</td>
        <td>integer</td>
    </tr>
    <tr>
        <th></th>
        <td>country_id</td>
        <td>foreignId('country_id')->constrained()->cascadeOnDelete()</td>
    </tr>
    <tr>
        <th></th>
        <td>name</td>
        <td>string</td>
    </tr>
    <tr>
        <th></th>
        <td>timestamp</td>
        <td></td>
    </tr>
</table>

<table>
    <tr>
        <th>cities</th>
        <td>id</td>
        <td>integer</td>
        <td></td>
    </tr>
    <tr>
        <th></th>
        <td>state_id</td>
        <td>foreignId('state_id')->constrained()->cascadeOnDelete()</td>
        <td>fillable</td>
    </tr>
    <tr>
        <th></th>
        <td>name</td>
        <td>string</td>
        <td>fillable</td>
    </tr>
    <tr>
        <th></th>
        <td>timestamp</td>
        <td></td>
        <td></td>
    </tr>
</table>

<table>
    <tr>
        <th>departments</th>
        <td>id</td>
        <td>integer</td>
        <td></td>
    </tr>
    <tr>
        <th></th>
        <td>name</td>
        <td>string</td>
        <td>fillable</td>
    </tr>
    <tr>
        <th></th>
        <td>timestamp</td>
        <td></td>
        <td></td>
    </tr>
</table>

### Relationships between Tables

#### Employees Table

- **country_id:** Foreign key referencing the `id` column in the `countries` table. *(Many employees can belong to one country)*
- **state_id:** Foreign key referencing the `id` column in the `states` table. *(Many employees can belong to one state)*
- **city_id:** Foreign key referencing the `id` column in the `cities` table. *(Many employees can belong to one city)*
- **department_id:** Foreign key referencing the `id` column in the `departments` table. *(Many employees can belong to one department)*

#### Countries Table

- No direct relationships.

#### States Table

- **country_id:** Foreign key referencing the `id` column in the `countries` table. *(One state belongs to one country, but a country can have many states)*
  - **Employees:** One-to-many relationship with the `employees` table through the `state_id` foreign key.

#### Cities Table

- **state_id:** Foreign key referencing the `id` column in the `states` table. *(One city belongs to one state, but a state can have many cities)*
  - **Employees:** One-to-many relationship with the `employees` table through the `city_id` foreign key.

#### Departments Table

- No direct relationships.
  - **Employees:** One-to-many relationship with the `employees` table through the `department_id` foreign key.
