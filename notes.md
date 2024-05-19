<h1 align="center">Employee Mangement System</h1>

- Create Project
    ```
    composer create-project laravel/laravel:^10.0 laravel-filament-employee-management
    ```

- Install Breeze
    ```
    composer require laravel/breeze --dev
    ```
    ```
    php artisan breeze:install
    ```
    ```
    npm install
    ```
    ```
    npm run dev
    ```
- Create Database
    - database name - filament_emp_db
    ```
    php artisan migrate
    ```
- Install Filament
    ```
    composer require filament/filament:"^3.2" -W
    ```
    ```
    php artisan filament:install --panels
    ```
    ```
    php artisan make:filament-user
    ```


- Fix login attempt
- Create Model for country, state, city, department, employee
- Make relationships
- Working with migrations
