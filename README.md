# Vehicle Management System 🚙🚚🛵

This is a Python-based graphical application that allows users to manage vehicles by adding details for different types of vehicles such as Cars, Trucks, and Motorcycles. It provides a user-friendly interface using the `tkinter` library and stores vehicle data in a MySQL database.

## 🚀Features

- Add vehicle details (license plate, make, model, year) for Cars, Trucks, and Motorcycles.
- Capture additional vehicle-specific details (e.g., number of doors for Cars, load capacity for Trucks, engine capacity for Motorcycles).
- Data is saved into a MySQL database.
- The application displays a thank you message when exiting.

## 🔧Requirements

- Python 3.x
- `tkinter` library (Usually included with Python)
- `mysql-connector-python` library
- MySQL database server

## 🛠️Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/vehicle-management-system.git
    cd vehicle-management-system
    ```

2. **Install the required libraries**:
    ```bash
    pip install -r requirements.txt
    ```

3. **Set up the MySQL database**:
    - Create a MySQL database named `vehicle_management`.
    - Ensure you have a table `vehicles` with the following structure:
      ```sql
      CREATE TABLE vehicles (
          id INT AUTO_INCREMENT PRIMARY KEY,
          license_plate VARCHAR(50),
          make VARCHAR(50),
          model VARCHAR(50),
          year INT,
          vehicle_type VARCHAR(20),
          num_doors INT,
          load_capacity INT,
          engine_capacity INT
      );
      ```

4. **Update the database connection settings**:
    In the `vehicle_management_system.py` file, update the `get_db_connection()` function with your MySQL credentials.

    ```python
    def get_db_connection():
        return mysql.connector.connect(
            host="localhost",
            user="root",  # Your MySQL username
            password="",  # Your MySQL password
            database="vehicle_management"
        )
    ```

## How to Run 🏃

1. After completing the setup, run the application:
    ```bash
    python vehicle_management_system.py
    ```

2. The GUI will open with options to select a vehicle type and input the vehicle details.

## User Interface 🚚🚗🏍️

- **Page 1**: Select the type of vehicle (Car, Truck, or Motorcycle).
  ![Screenshot 2025-01-09 171327](https://github.com/user-attachments/assets/25b2d4ef-e918-4a87-af13-10406d85b391)

  
- **Page 2**: Input vehicle details such as license plate, make, model, year, and any vehicle-specific information. 🏎️
![Screenshot 2025-01-09 171344](https://github.com/user-attachments/assets/8c1921d1-1281-461a-92ed-c454867ad277)


- After submission, the vehicle is added to the database, and the user is returned to Page 1. 🛻🚗🚴‍♂️
![Screenshot 2025-01-09 171450](https://github.com/user-attachments/assets/5bd2456f-1726-4258-8ecf-2e46d6f306ed)

## Exiting the Application 🔚

Click on the "Exit" button at any point to exit the application. A thank you message will be displayed before the application closes.
![Screenshot 2025-01-09 171504](https://github.com/user-attachments/assets/dee91b8d-f551-46e4-9482-07d9592786f0)

🥳Thank You for using this code.
