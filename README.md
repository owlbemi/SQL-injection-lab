# SQL-injection-lab (SQL Injection Attack Lab by SEED LAB)
## Procedure
I've followed instructions and lab report from:
- https://seedsecuritylabs.org/Labs_20.04/Web/Web_SQL_Injection/
- https://seedsecuritylabs.org/labsetup.html

## Tasks
1. Simple SQL injection from command line and dialogue box
2. Using complex SQL injection using ``WHERE`` and ``#`` (command block)
3. Test security API (countermeasure) regarding ``mysql::multi_query()``
4. Use of ``SELECT`` and ``WHERE`` command to change values in the database
5. Analyse ``.php`` file of the website in order to get what encoding one used for password
6. Bypassing defense SQL commands by editing the ``.php`` file with the following commands:

```
$stmt = $conn->prepare("SELECT name, local, gender
FROM USER_TABLE
WHERE id = ? and password = ? ");
// Bind parameters to the query
$stmt->bind_param("is", $id, $pwd);
$stmt->execute();
$stmt->bind_result($bind_name, $bind_local, $bind_gender);
$stmt->fetch();
```
