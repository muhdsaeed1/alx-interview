

# Lockboxes

## Description
The Lockboxes project is a secure storage solution for sensitive items. It provides a Python-based implementation for managing and accessing lockboxes, allowing users to store their valuables with peace of mind. This readme file provides an overview of the project and instructions for setting it up and using it.

## Features
- User registration and authentication
- Creation, deletion, and management of lockboxes
- Secure encryption and decryption of lockbox contents
- Access control and permissions management
- Activity logging for auditing purposes

## Installation
1. Clone the repository: `git clone https://github.com/your-username/lockboxes.git`
2. Navigate to the project directory: `cd lockboxes`
3. Install the required dependencies: `pip install -r requirements.txt`
4. Configure the environment variables:
   - Create a `.env` file in the project directory and provide the necessary configurations (e.g., database connection URL, secret keys).
5. Start the application: `python app.py`
6. Access the application in your browser at `http://localhost:5000`

## Usage
1. Register a new user account or log in with existing credentials.
2. Upon successful login, you will be redirected to the dashboard.
3. On the dashboard, you can create a new lockbox by providing a name and optional description.
4. Once a lockbox is created, you can add items to it by specifying a name, description, and uploading a file (optional).
5. To view the contents of a lockbox, click on its name on the dashboard. You will be prompted to enter the lockbox's encryption key.
6. After entering the correct encryption key, the lockbox contents will be decrypted and displayed.
7. You can delete a lockbox by selecting it on the dashboard and clicking the delete button.
8. Logout from the application when you're finished.

## Contact
If you have any questions or inquiries, you can contact the project maintainer at olayinkasaheed32@gmail.com
