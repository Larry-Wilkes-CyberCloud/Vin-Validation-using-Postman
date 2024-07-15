<div>
  <h2>QA Engineer Portfolio: Vin Validation Using Postman</h2>
  <p><strong>Company:</strong> General Insurance INC.</p>
  <p>
    As a QA Engineer at General Insurance INC., I have conducted thorough test cases to verify the validation of vehicle VIN numbers. This project focused on ensuring that the vehicle creation endpoint correctly handles various scenarios related to VIN number validation, maintaining data integrity, and adhering to the required specifications.
  </p>
  <h3>Test Case Outline:</h3>
  <ol>
    <li>Verify that the user is able to successfully save driver information with a valid vin number. Status code 201 received.</li>
    <li>Send a request with vin as alphanumeric characters, request should process successfully.</li>
    <li>Send a request with vin greater than 20 characters, error message received with status code 400.</li>
    <li>Send a request with special characters in the vin number, error message received with status code 400.</li>
  </ol>
  <h3>Test Case Results:</h3>
  
  <!-- Test Case 1 -->
  <table border="1">
    <thead>
      <tr>
        <th colspan="4">Test Case ID: TC01</th>
      </tr>
      <tr>
        <th>API Body</th>
        <th>Expected Result</th>
        <th>Actual Result</th>
        <th>Status Code</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>
          {
            "year": "1989",
            "Make": "Mazda",
            "Trim": "Touring",
            "MIleage": 98000,
            "numberplate": "PQR456",
            "registeredstate": "Colorado",
            "createdDate": "2014-11-12T00:00:00.000Z",
            "vin": "JM3KE2CY3E1234567",
            "Model": "CX-5",
            "Color": "Red"
          }
        </td>
        <td>Verify that the user can save driver information successfully with a valid vin number. Status code 201 received.</td>
        <td>I verified that the user can save driver information with a valid vin number. Status code 201 received.</td>
        <td>Status code 201 received.</td>
      </tr>
      <tr>
        <td colspan="4"><img src="https://github.com/Larry-Wilkes-CyberCloud/Vin-Validation-using-Postman/assets/93053015/91a8b702-3ac5-48ca-9a93-f9297a0a4a7d" width="1000" height="500" alt="Test Case 1"></td>
      </tr>
    </tbody>
  </table>
  <br>
  
  <!-- Test Case 2 -->
  <table border="1">
    <thead>
      <tr>
        <th colspan="4">Test Case ID: TC02</th>
      </tr>
      <tr>
        <th>API Body</th>
        <th>Expected Result</th>
        <th>Actual Result</th>
        <th>Status Code</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>
          {
            "year": "2006",
            "Make": "Subaru",
            "Trim": "Limited",
            "MIleage": 105000,
            "numberplate": "MNO321",
            "registeredstate": "Washington",
            "createdDate": "2015-09-25T00:00:00.000Z",
            "vin": "4S4BRBLC6F321456",
            "Model": "Outback",
            "Color": "Green"
          }
        </td>
        <td>Send a request with vin as alphanumeric characters, request should process successfully. Status code 201 received.</td>
        <td>I verified that the user can save vin numbers with alphanumeric characters. Status code 201 received.</td>
        <td>Status code 201 received.</td>
      </tr>
      <tr>
        <td colspan="4"><img src="https://github.com/Larry-Wilkes-CyberCloud/Vin-Validation-using-Postman/assets/93053015/dbf9961e-ea67-4309-8edf-334f247e68c6" width="1000" height="500" alt="Test Case 2"></td>
      </tr>
    </tbody>
  </table>
  <br>
  
  <!-- Test Case 3 -->
  <table border="1">
    <thead>
      <tr>
        <th colspan="4">Test Case ID: TC03</th>
      </tr>
      <tr>
        <th>API Body</th>
        <th>Expected Result</th>
        <th>Actual Result</th>
        <th>Status Code</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>
          {
            "year": "2022",
            "Make": "Toyota",
            "Trim": "LTZ",
            "MIleage": 23236,
            "numberplate": "KUO138",
            "registeredstate": "California",
            "createdDate": "2022-06-18T00:00:00.000Z",
            "vin": 695277816991111122000000002223333333,
            "Model": "MRK",
            "Color": "White"
          }
        </td>
        <td>Send a request with vin greater than 20 characters, error message received with status code 400.</td>
        <td>I sent a request with a vin greater than 20 characters, error message received with status code 400.</td>
        <td>Status code 400 received.</td>
      </tr>
      <tr>
        <td colspan="4"><img src="https://github.com/Larry-Wilkes-CyberCloud/Vin-Validation-using-Postman/assets/93053015/4e2afabd-4685-4790-909a-326addf81cfe" height="500" alt="Test Case 3"></td>
      </tr>
    </tbody>
  </table>
  <br>
  
  <!-- Test Case 4 -->
  <table border="1">
    <thead>
      <tr>
        <th colspan="4">Test Case ID: TC04</th>
      </tr>
      <tr>
        <th>API Body</th>
        <th>Expected Result</th>
        <th>Actual Result</th>
        <th>Status Code</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>
          {
            "year": "1998",
            "Make": "Volkswagen",
            "Trim": "SE",
            "MIleage": 120000,
            "numberplate": "STU789",
            "registeredstate": "Oregon",
            "createdDate": "2013-07-20T00:00:00.000Z",
            "vin": 1VWBP7A35DC1234!6,
            "Model": "Passat",
            "Color": "White"
          }
        </td>
        <td>Send a request with a special characters in the vin number, error message received with status code 400.</td>
        <td>I sent a request with a special character in the vin number, error message status code 400 received.</td>
        <td>Status code 400 received.</td>
      </tr>
      <tr>
        <td colspan="4"><img src="https://github.com/Larry-Wilkes-CyberCloud/Vin-Validation-using-Postman/assets/93053015/ff36db10-6868-46be-846e-00c6aedde1ca" width="1000" height="500" alt="Test Case 4"></td>
      </tr>
    </tbody>
  </table>
  <br>
</div>
