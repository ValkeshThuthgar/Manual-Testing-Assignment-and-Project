+---------+-------------+---------------------+-------------------------------+-----------------------------------+-----------------+---------------+--------+
| TC ID   | Module      | Test Scenario       | Test Steps                    | Expected Result                   | Test Data       | Actual Result | Status |
+---------+-------------+---------------------+-------------------------------+-----------------------------------+-----------------+---------------+--------+
| TC_001  | Login       | Valid Login Check   | 1. Enter valid email.         | User should be redirected to home | test@email.com  | As Expected   | PASS   |
|         |             |                     | 2. Enter valid password.      | page successfully.                | Pass@123        |               |        |
|         |             |                     | 3. Click Login button.        |                                   |                 |               |        |
+---------+-------------+---------------------+-------------------------------+-----------------------------------+-----------------+---------------+--------+
| TC_002  | Login       | Invalid Password    | 1. Enter valid email.         | System should show error message: | test@email.com  | System        | FAIL   |
|         |             |                     | 2. Enter WRONG password.      | "Invalid credentials".            | WrongPass       | Crashed       |        |
|         |             |                     | 3. Click Login button.        |                                   |                 |               |        |
+---------+-------------+---------------------+-------------------------------+-----------------------------------+-----------------+---------------+--------+
