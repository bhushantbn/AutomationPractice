Login validation Scenario Practice Form :-
| #  | **Scenario**                        | **Username** | **Password**                | **Expected Result / Message**                                      |
| -- | ----------------------------------- | ------------ | --------------------------- | ------------------------------------------------------------------ |
| 1  | Empty password                      | `user1`      | *(blank)*                   | `Password is required.`                                            |
| 2  | Password below minimum length       | `user1`      | `A1@a`                      | `Password must be at least 8 characters.`                          |
| 3  | Password above maximum length       | `user1`      | `A1@` + 50 chars            | `Password must not exceed 20 characters.`                          |
| 4  | No uppercase letter                 | `user1`      | `password1@`                | `Password must contain at least one uppercase letter.`             |
| 5  | No lowercase letter                 | `user1`      | `PASSWORD1@`                | `Password must contain at least one lowercase letter.`             |
| 6  | No digit                            | `user1`      | `Password@`                 | `Password must contain at least one digit.`                        |
| 7  | No special character                | `user1`      | `Password1`                 | `Password must contain at least one special character (!@#$%^&*).` |
| 8  | Password contains spaces            | `user1`      | `Password 1@`               | `Password must not contain spaces.`                                |
| 9  | Password contains only spaces       | `  `      | `     `                     | `Password is required.`                                            |
| 10 | SQL injection-like input            | `user1`      | `' OR '1'='1`               | `SQL-like patterns are not allowed in password.`                   |
| 11 | HTML/script injection               | `user1`      | `<script>alert(1)</script>` | `Scripts are not allowed in password.`                             |
| 12 | Common/weak password                | `user1`      | `password123`               | `Password is too common or weak.`                                  |
| 13 | Password same as username           | `Admin123`   | `Admin123`                  | `Password must not be the same as username.`                       |
| 14 | Correct password (for success case) | `testuser`   | `Test@1234`                 | `Login successful (validation passed)`                             |
