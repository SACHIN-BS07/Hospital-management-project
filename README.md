# Hospital-management-project

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Hospital Management System</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <style>
        body { font-family: Arial, sans-serif; background: #f4f6f8; margin: 0; }
        header { background: #1976d2; color: #fff; padding: 20px 0; text-align: center; }
        nav { background: #1565c0; padding: 10px 0; text-align: center; }
        nav a { color: #fff; margin: 0 15px; text-decoration: none; font-weight: bold; }
        main { max-width: 900px; margin: 30px auto; background: #fff; padding: 30px; border-radius: 8px; box-shadow: 0 2px 8px #ccc; }
        h2 { color: #1976d2; }
        table { width: 100%; border-collapse: collapse; margin-top: 20px; }
        th, td { border: 1px solid #ddd; padding: 10px; text-align: left; }
        th { background: #e3f2fd; }
        form { margin-top: 30px; }
        label { display: block; margin: 10px 0 5px; }
        input, select { width: 100%; padding: 8px; margin-bottom: 15px; border: 1px solid #ccc; border-radius: 4px; }
        button { background: #1976d2; color: #fff; border: none; padding: 10px 20px; border-radius: 4px; cursor: pointer; }
        button:hover { background: #1565c0; }
        footer { text-align: center; padding: 15px 0; background: #e3f2fd; margin-top: 40px; }
    </style>
</head>
<body>
    <header>
        <h1>Hospital Management System</h1>
    </header>
    <nav>
        <a href="#">Dashboard</a>
        <a href="#">Patients</a>
        <a href="#">Doctors</a>
        <a href="#">Appointments</a>
        <a href="#">Billing</a>
    </nav>
    <main>
        <h2>Patient Registration</h2>
        <form id="patientForm">
            <label for="pname">Patient Name</label>
            <input type="text" id="pname" name="pname" required>
            <label for="age">Age</label>
            <input type="number" id="age" name="age" required>
            <label for="gender">Gender</label>
            <select id="gender" name="gender" required>
                <option value="">Select</option>
                <option>Male</option>
                <option>Female</option>
                <option>Other</option>
            </select>
            <label for="disease">Disease</label>
            <input type="text" id="disease" name="disease" required>
            <button type="submit">Register Patient</button>
        </form>
        <h2>Patient List</h2>
        <table id="patientsTable">
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Age</th>
                    <th>Gender</th>
                    <th>Disease</th>
                </tr>
            </thead>
            <tbody>
               // Patient rows will appear here //
            </tbody>
        </table>
    </main>
    <footer>
        &copy; 2025 Hospital Management System
    </footer>
    <script>
        // Simple JS to add patient to table
        document.getElementById('patientForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const name = document.getElementById('pname').value;
            const age = document.getElementById('age').value;
            const gender = document.getElementById('gender').value;
            const disease = document.getElementById('disease').value;
            const table = document.getElementById('patientsTable').getElementsByTagName('tbody')[0];
            const newRow = table.insertRow();
            newRow.insertCell(0).innerText = name;
            newRow.insertCell(1).innerText = age;
            newRow.insertCell(2).innerText = gender;
            newRow.insertCell(3).innerText = disease;
            document.getElementById('patientForm').reset();
        });
         </script>
</body>
</html>
