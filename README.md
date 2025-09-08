<h1 align="center">
  <img src="https://github.com/XanderSteyn/xandersteyn/blob/main/IGNORE/Headers/Tasks/Databases.svg" width="100%" height="130px" alt="Databases - CLI Bookstore Inventory Manager"/>
</h1>

<img src="https://github.com/XanderSteyn/xandersteyn/blob/main/IGNORE/Headers/Table%20of%20Contents.svg" alt="Table of Contents" height="25px"/>

- [**Features**](#features)
- [**Tech Stack**](#tech-stack)
- [**Setup & Installation**](#setup)
- [**Database Schema**](#database-schema)
- [**Security**](#security)
- [**Contributing**](#contributing)
- [**License**](#license)

<h1></h1>

<a name="features"></a>
<img src="https://github.com/XanderSteyn/xandersteyn/blob/main/IGNORE/Headers/Repos/Features.svg" alt="Features" height="25px"/>

| Feature                | Description                                                                  |
|------------------------|------------------------------------------------------------------------------|
| Add Books              | Register new books with title, author, and quantity                          |
| Update Books           | Edit book details, including title, author, and stock                        |
| Delete Books           | Remove books from inventory with confirmation                                |
| Search Books           | Find books by ID or partial title match                                      |
| View Inventory         | Display all books in table or detailed list format                           |
| Author Management      | Add and update author details, with enforced foreign key relationships       |
| Data Validation        | Comprehensive input validation and error handling                            |
| Cross-Platform         | Works on Windows, macOS, and Linux                                           |

<h1></h1>

<a name="tech-stack"></a>
<img src="https://github.com/XanderSteyn/xandersteyn/blob/main/IGNORE/Headers/Tech%20Stack.svg" alt="Tech Stack" height="25px"/>

- **Language:** Python 3.11+
- **Database:** SQLite (via `sqlite3`)
- **CLI UI:** Standard input/output, enhanced with [`tabulate`](https://pypi.org/project/tabulate/) for tables

<h1></h1>

<a name="setup"></a>
<img src="https://github.com/XanderSteyn/xandersteyn/blob/main/IGNORE/Headers/Repos/Setup%20Instructions.svg" alt="Setup & Installation" height="30px"/>

#### 1. Clone the repository
```bash
git clone https://github.com/XanderSteyn/HyperionDev.Bookstore/
```

#### 2. Change to the project directory
```bash
cd "HyperionDev.Bookstore"
```

#### 3. Create a virtual environment
- **Windows:**
  ```powershell
  python -m venv venv
  ```
- **macOS/Linux:**
  ```bash
  python3 -m venv venv
  ```

#### 4. Activate the virtual environment
- **Windows (Command Prompt):**
  ```cmd
  .\venv\Scripts\activate.bat
  ```
- **Windows (PowerShell):**
  ```powershell
  .\venv\Scripts\Activate.ps1
  ```
- **macOS/Linux:**
  ```bash
  source ./venv/bin/activate
  ```

#### 5. Install dependencies
```bash
pip install -r requirements.txt
```

#### 6. Run the application
```sh
python shelf_track.py
```

<h1></h1>

<a name="database-schema"></a>
<img src="https://github.com/XanderSteyn/xandersteyn/blob/main/IGNORE/Headers/Repos/DatabaseSchema.svg" alt="Database Schema" height="25px"/>

| Table   | Fields                                                                                                                                                         |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| author  | `id (INTEGER, PRIMARY KEY)`<br> `name (TEXT, NOT NULL)`<br> `country (TEXT, NOT NULL)`                                                                               |
| book    | `id (INTEGER, PRIMARY KEY)`<br> `title (TEXT, NOT NULL)`<br> `author_id (INTEGER, NOT NULL, FOREIGN KEY → author.id)`<br> `qty (INTEGER, NOT NULL, CHECK qty >= 0)` |

**Initial Data:**  
~ Populated with classic authors and books on first run.

<h1></h1>

<a name="security"></a>
<img src="https://github.com/XanderSteyn/xandersteyn/blob/main/IGNORE/Headers/Repos/Security.svg" alt="Security" height="30px"/>

- **Input Validation:** All user input is validated for type, length, and constraints.
- **SQL Injection Protection:** Uses parameterized queries throughout.
- **Data Integrity:** Foreign key constraints and transaction rollbacks on error.
- **Graceful Error Handling:** Handles database and user input errors robustly.

<h1></h1>

<a name="contributing"></a>
<img src="https://github.com/XanderSteyn/xandersteyn/blob/main/IGNORE/Headers/Repos/Contributing.svg" alt="Contributing" height="30px"/>

1. Fork the repository and create a feature branch.
2. Follow PEP8 and project code style (see `.flake8` config)
3. Write tests for new features and bug fixes.
4. Submit a pull request with a clear description.

<h1></h1>

<a name="license"></a>
<img src="https://github.com/XanderSteyn/xandersteyn/blob/main/IGNORE/Headers/License.svg" alt="License" height="25px"/>

This repository is protected by a custom license. See the [LICENSE](LICENSE) file for details.  
Unauthorized copying or submission of this work for academic purposes is prohibited.
