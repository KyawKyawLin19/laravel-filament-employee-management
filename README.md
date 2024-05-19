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
    </tr>
    <tr>
        <th></th>
        <td>first_name</td>
    </tr>
    <tr>
        <th></th>
        <td>last_name</td>
    </tr>
    <tr>
        <th></th>
        <td>address</td>
    </tr>
    <tr>
        <th></th>
        <td>department_id</td>
    </tr>
    <tr>
        <th></th>
        <td>city_id</td>
    </tr>
    <tr>
        <th></th>
        <td>state_id</td>
    </tr>
    <tr>
        <th></th>
        <td>country_id</td>
    </tr>
    <tr>
        <th></th>
        <td>zip_code</td>
    </tr>
    <tr>
        <th></th>
        <td>birth_date</td>
    </tr>
    <tr>
        <th></th>
        <td>date_hired</td>
    </tr>
    <tr>
        <th></th>
        <td>timestamp</td>
    </tr>
</table>

<table>
    <tr>
        <th>countries</th>
        <td>id</td>
    </tr>
    <tr>
        <th></th>
        <td>country_code</td>
    </tr>
    <tr>
        <th></th>
        <td>name</td>
    </tr>
    <tr>
        <th></th>
        <td>timestamp</td>
    </tr>
</table>

<table>
    <tr>
        <th>states</th>
        <td>id</td>
    </tr>
    <tr>
        <th></th>
        <td>country_id</td>
    </tr>
    <tr>
        <th></th>
        <td>name</td>
    </tr>
    <tr>
        <th></th>
        <td>timestamp</td>
    </tr>
</table>

<table>
    <tr>
        <th>cities</th>
        <td>id</td>
    </tr>
    <tr>
        <th></th>
        <td>state_id</td>
    </tr>
    <tr>
        <th></th>
        <td>name</td>
    </tr>
    <tr>
        <th></th>
        <td>timestamp</td>
    </tr>
</table>

<table>
    <tr>
        <th>departments</th>
        <td>id</td>
    </tr>
    <tr>
        <th></th>
        <td>name</td>
    </tr>
    <tr>
        <th></th>
        <td>timestamp</td>
    </tr>
</table>
