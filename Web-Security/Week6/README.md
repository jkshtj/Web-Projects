# Project 6 - Globitek Authentication and Login Throttling

Time spent: **2** hours spent in total

## User Stories

The following **required** functionality is completed:

1\. "staff/users/new.php" and "staff/users/edit.php"
  * [X]  Form with inputs for "Password" and "Confirm Password"
  * [X]  Strong password requirements text

2\. Data validations
  * [X]  Returns an error if password or confirm_password are blank.
  * [X]  Returns an error if password and confirm_password do not match.
  * [X]  Returns an error if password is not at least 12 characters long.
  * [X]  Returns an error if password does not meet character requirements.
  * [X]  Returns any errors related to other validations already on the user.

3\. Saving a user
  * [X]  Encrypts the password
  * [X]  Stores the password in the database

4\. Login page
  * [X]  Verify the correct password.
  * [X]  Do not create a User Enumeration vulnerability.

5\. If a user fails to log in:
  * [X]  Record the failed login for the first 5 attempts.
  * [X]  Return a "too many failed logins" message after 5 attempts.
  * [X]  Future attempts will show the number of minutes remaining in the lockout.
  * [X]  After the lockout period, the failed logins count resets to 0.

6\. After any successful login:
  * [X]  Set the failed_logins.count for the username to 0.

7\. SQLi and XSS
  * [X]  Do not introduce any SQLI Injection and Cross-Site Scripting vulnerabilities.

The following advanced user stories are optional:

* Bonus Objective 1\.
  * [ ]  Identify the subtle Username Enumeration weakness. Include a short description of how the code could be modified to be more secure below:

* Bonus Objective 2\.
  * [ ]  User password validations only run when the password is not blank.
  * [ ]  `update_user` only encrypts and updates the password when the password is not blank.

* Bonus Objective 3\.
  * [ ]  Create a new user using cost 10.
  * [ ]  Set bcrypt "cost" parameter to 11 (for both insert and update).
  * [ ]  Try to login with the "cost 10" user.
  * [ ]  Briefly describe why login still works even after the cost is changed:

* Bonus Objective 4\.
  * [ ]  Add "Previous password" to "public/staff/users/edit.php"
  * [ ]  Validate the previous password before allowing the password to be updated.
  * [ ]  Require previous password only if new password is being updated (if also completing Bonus Objective 2).

* Advanced Objective 1\.
  * [ ]  Implement `password_hash()` on your own as `my_password_hash()`.
  * [ ]  Implement `password_verify()` on your own as `my_password_verify()`.

* Advanced Objective 2\.
  * [ ]  Write `generate_strong_password()`
  * [ ]  Add a suggestion for a 12-character strong password to the new and edit user pages.

## Video Walkthrough

Here's a walkthrough of implemented user stories:

<img src='http://i.imgur.com/OSAT0Nt.gif' title='Video Walkthrough' width='' alt='Video Walkthrough' />

GIF created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while building the app.

## License

    Copyright [2017] [Kshitij Jain]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
>>>>>>> 26f111a892938590745fe65696bbf72e1105bddd