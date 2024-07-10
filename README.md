<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <h1>Vin-Validation-Using-Postman</h1>
    <p>
        As a QA Engineer at General Insurance INC., I have conducted thorough test cases to verify the validation of vehicle VIN numbers. This project focused on ensuring that the vehicle creation endpoint correctly handles various scenarios related to VIN number validation, maintaining data integrity, and adhering to the required specifications.
    </p>
    <h2>Requirement:</h2>
    <p>The <strong>vin</strong> (Vehicle Identification Number) field must adhere to the following criteria:</p>
    <ul>
        <li>It must be provided.</li>
        <li>It must be alphanumeric only.</li>
        <li>Special characters are not allowed.</li>
        <li>Maximum length is 20 characters.</li>
        <li>For successful attempts, a status code of 201 is received.</li>
        <li>For errors, a status code of 400 is received.</li>
    </ul>
    <br>
    <h2>Test Case 1</h2>
    <table>
        <tr>
            <th>API Body</th>
            <th>Expected Result</th>
            <th>Actual Result</th>
        </tr>
        <tr>
            <td>
                { <br>
                "year": "1989", <br>
                "Make": "Mazda", <br>
                "Trim": "Touring", <br>
                "MIleage": 98000, <br>
                "numberplate": "PQR456", <br>
                "registeredstate": "Colorado", <br>
                "createdDate": "2014-11-12T00:00:00.000Z", <br>
                "vin": "JM3KE2CY3E1234567", <br>
                "Model": "CX-5", <br>
                "Color": "Red" <br>
                }
            </td>
            <td>Verify that the user can save driver information successfully with a valid vin number. Status code 201 received.</td>
            <td>I verified that the user can save driver information with a valid vin number. Status code 201 received.</td>
        </tr>
    </table>
    <br>
    <img src="https://github.com/Larry-Wilkes-CyberCloud/Vin-Validation-using-Postman/assets/93053015/c7d9d436-a935-4952-aee1-fad8a640375c" width="1000" height="500" alt="GitHub Asset">
</body>
</html>
