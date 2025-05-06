# Encryption Tool
This command-line tool encrypts and decrypts individual files using AES encryption in CBC mode. It includes password protection to restrict access.


## Features
- Encrypt a single file.
- Decrypt a single file.
- Password-protected access.
- Option to generate a random password during setup.


## Requirements
- Python 3.6
- pycryptodome library
- termcolor library


## Installation
1. Clone or Download the Project:
  - If hosted on a repository, use:
  `git clone <repository-url>`
  - Otherwise, download and extract the project files.
3. Navigate to the Project Directory:
   `cd encryption_tool`
4. Install Dependencies:
  `pip install pycryptodome termcolor`


## Usage
1. Initial Setup:
   - Run the script for the first time:
     `python encryption_tool.py`
   - You will be prompted to set up a password:
       - Choose to generate a random password or enter one manually.
       - The password will be encrypted and saved as password.txt.enc.
2. Running the Tool:
     - Launch the script:
       `python encryption_tool.py`
     - Enter the password to access the tool.
     - Select an option from the menu:
         - Encrypt a file: Enter the name of the file to encrypt (e.g., example.txt).
         - Decrypt a file: Enter the name of the encrypted file (e.g., example.txt.enc).
         - Exit: Close the tool.         
3. Example:
  - To encrypt example.txt:
     - Select option 1 and enter example.txt.
     - The encrypted file will be saved as example.txt.enc.
  - To decrypt example.txt.enc:
     - Select option 2 and enter example.txt.enc.
     - The decrypted file will be restored as example.txt.


## Implementation Details
1. Encryption: Uses AES in CBC mode with a hardcoded key. Files are padded to the AES block size and encrypted, then saved with a .enc extension.
2. Decryption: Reverses the encryption process, removing the .enc extension upon successful decryption.
3. Password Authentication: The tool requires a password to access its features. The password is stored in an encrypted file (password.txt.enc) and verified each time the tool is run.

 
## Future Improvements
1. Support for file paths beyond the current directory.
2. Batch encryption/decryption of multiple files.
3. Improved key management and security.

