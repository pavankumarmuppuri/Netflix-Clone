# Netflix Clone App
This is a Flask web application that serves as a clone of Netflix, allowing users to sign in, register, and access movies. 


### Working

https://github.com/pavankumarmuppuri/Netflix-Clone/assets/155610590/2e4add6b-10a4-4558-9b78-07662d470e83

## Setup

1. **Clone the Repository**: Clone this repository to your local machine using `git clone`.

2. **Database Configuration and URI**: Set up a PostgreSQL database for the application.<br> You can use tools like pgAdmin or the command line to create a new database and user.<br> Obtain the URI for connecting to your PostgreSQL database. <br>It should look like `postgresql://username:password@localhost/database_name`, where:
    - `username`: Your PostgreSQL username
    - `password`: Your PostgreSQL password
    - `localhost`: The host where your database is running (typically `localhost` for local development)
    - `database_name`: The name of your database

    **Replace Database URI**: Replace the default database URI in `app.py` with your own database connection details. Modify the following line:

    ```python
    app.config['SQLALCHEMY_DATABASE_URI'] = 'postgresql://username:password@localhost/database_name'
    ```

    Replace `username`, `password`, and `database_name` with your actual database credentials.


3. **Install Dependencies**: Install the required Python dependencies using `pip install -r requirements.txt`.

4. **Initialize Database**: Run the following command to initialize the database schema:

    ```bash
    python app.py db upgrade
    ```

5. **Run the Application**: Start the Flask application by running `python app.py`.

6. **Access the Application**: Access the application in your web browser at `http://localhost:5000`.


## Features

- **User Authentication**: Users can sign in, register, and log out securely.
- **Superuser Privileges**: Superusers have additional privileges such as managing users.
- **Database Integration**: Uses PostgreSQL database for storing user data.
- **Restricted Access to Movies**: Movie access is limited to logged-in users only. Only authenticated users can access and watch movies, ensuring a secure and personalized viewing experience.

