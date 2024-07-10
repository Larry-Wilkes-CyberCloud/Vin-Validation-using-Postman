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
    <img src="https://github.com/Larry-Wilkes-CyberCloud/Vin-Validation-using-Postman/assets/93053015/91a8b702-3ac5-48ca-9a93-f9297a0a4a7d"width="1000" height="500" alt="Test Case 1">
    <br>
    <h2>Test Case 2</h2>
    <table>
        <tr>
            <th>API Body</th>
            <th>Expected Result</th>
            <th>Actual Result</th>
        </tr>
        <tr>
            <td>
                { <br>
                "year": "2006", <br>
                "Make": "Subaru", <br>
                "Trim": "Limited", <br>
                "MIleage": 105000, <br>
                "numberplate": "MNO321", <br>
                "registeredstate": "Washington", <br>
                "createdDate": "2015-09-25T00:00:00.000Z", <br>
                "vin": "4S4BRBLC6F321456", <br>
                "Model": "Outback", <br>
                "Color": "Green" <br>
                }
            </td>
            <td>Send a request with vin as alphanumeric characters, request should process successfully. Status code 201 received.</td>
            <td>I verified that the user can save vin numbers with alphanumeric characters. Status code 201 received.</td>
        </tr>
    </table>
    <br>
    <img src="https://github.com/Larry-Wilkes-CyberCloud/Vin-Validation-using-Postman/assets/93053015/dbf9961e-ea67-4309-8edf-334f247e68c6" width="1000" height="500" alt="Test Case 2">
    <br>
    <h2>Test Case 3</h2>
    <table>
        <tr>
            <th>API Body</th>
            <th>Expected Result</th>
            <th>Actual Result</th>
        </tr>
        <tr>
            <td>
                { <br>
                "year": "2022", <br>
                "Make": "Toyota", <br>
                "Trim": "LTZ", <br>
                "MIleage": 23236, <br>
                "numberplate": "KUO138", <br>
                "registeredstate": "California", <br>
                "createdDate": "2022-06-18T00:00:00.000Z", <br>
                "vin": 695277816991111122000000002223333333, <br>
                "Model": "MRK", <br>
                "Color": "White" <br>
                }
            </td>
            <td>Send a request with vin greater than 20 characters, error message received with status code 400.</td>
            <td>I sent a request with a vin greater than 20 characters, error message received with status code 400.</td>
        </tr>
    </table>
    <br>
    <img src="https://github.com/Larry-Wilkes-CyberCloud/Vin-Validation-using-Postman/assets/93053015/4e2afabd-4685-4790-909a-326addf81cfe" height="500" alt="Test Case 3">
    <br>
    <h2>Test Case 4</h2>
    <table>
        <tr>
            <th>API Body</th>
            <th>Expected Result</th>
            <th>Actual Result</th>
        </tr>
        <tr>
            <td>
                { <br>
                "year": "1998", <br>
                "Make": "Volkswagen", <br>
                "Trim": "SE", <br>
                "MIleage": 120000, <br>
                "numberplate": "STU789", <br>
                "registeredstate": "Oregon", <br>
                "createdDate": "2013-07-20T00:00:00.000Z", <br>
                "vin": 1VWBP7A35DC1234!6, <br>
                "Model": "Passat", <br>
                "Color": "White" <br>
                }
            </td>
            <td>Send a request with a special characters in the vin number, error message received with status code 400.</td>
            <td>I sent a request with a special character in the vin number, error message status code 400 received. </td>
        </tr>
    </table>
    <br>
    <img src="https://github.com/Larry-Wilkes-CyberCloud/Vin-Validation-using-Postman/assets/93053015/ff36db10-6868-46be-846e-00c6aedde1ca" width="1000" height="500" alt="Test Case 4">
</body>
</html>
```

