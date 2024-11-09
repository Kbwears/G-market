# G-market
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vehicle Registration & License Services</title>
    <link rel="stylesheet" href="styles.css"> <!-- Link to your external CSS file for styling -->
    <script src="script.js" defer></script> <!-- Link to your JavaScript file for dynamic interactions -->
</head>

<body>
    <!-- Header Section -->
    <header>
        <div class="logo">
            <h1>Vehicle Registration & License Services</h1>
        </div>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#login">Login</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Home Section -->
    <section id="home">
        <h2>Welcome to the Vehicle Registration and Licensing Platform</h2>
        <p>Your one-stop solution for vehicle registration, document renewal, and more. We connect vehicle owners with authorities, insurance agents, and other service providers.</p>
    </section>

    <!-- Services Section -->
    <section id="services">
        <h2>Our Services</h2>
        <ul>
            <li>Vehicle Registration & Change of Ownership</li>
            <li>Vehicle License Renewal</li>
            <li>Road Worthiness Inspection</li>
            <li>Hackney and Stage Carriage Permits</li>
            <li>Insurance Processing</li>
            <li>Proof of Ownership</li>
            <li>Other Custom Services (Specify upon Request)</li>
        </ul>
    </section>

    <!-- Login Section -->
    <section id="login">
        <h2>User Login</h2>
        <form action="login.php" method="POST" enctype="multipart/form-data">
            <div>
                <label for="email">Email Address:</label>
                <input type="email" id="email" name="email" required>
            </div>
            <div>
                <label for="national_id">National ID (e.g., NIN, Driver's License, International Passport):</label>
                <input type="file" id="national_id" name="national_id" accept="image/*" required>
            </div>
            <div>
                <label for="face_verification">Face Verification (Upload Selfie):</label>
                <input type="file" id="face_verification" name="face_verification" accept="image/*" required>
            </div>
            <div>
                <label for="account_number">Bank Account Number:</label>
                <input type="text" id="account_number" name="account_number" required>
            </div>
            <div>
                <label for="account_name">Account Name (Must Match ID):</label>
                <input type="text" id="account_name" name="account_name" required>
            </div>
            <button type="submit">Login</button>
        </form>
    </section>

    <!-- Vehicle Registration Section -->
    <section id="vehicle-registration">
        <h2>Vehicle Registration & Document Upload</h2>
        <form action="submit_registration.php" method="POST" enctype="multipart/form-data">
            <div>
                <label for="vehicle_type">Vehicle Type:</label>
                <select id="vehicle_type" name="vehicle_type" required>
                    <option value="car">Car</option>
                    <option value="motorcycle">Motorcycle</option>
                    <option value="bus">Bus</option>
                </select>
            </div>
            <div>
                <label for="vehicle_documents">Upload Vehicle Documents:</label>
                <input type="file" id="vehicle_documents" name="vehicle_documents[]" multiple required>
            </div>
            <div>
                <label for="payment">Payment Amount:</label>
                <input type="number" id="payment" name="payment" required>
            </div>
            <button type="submit">Submit Registration</button>
        </form>
    </section>

    <!-- Admin Section (To Be Accessed by Admins Only) -->
    <section id="admin-dashboard">
        <h2>Admin Dashboard</h2>
        <p>Here admins can handle user negotiations with licensing authorities and insurance agents.</p>
        <button onclick="window.location.href='admin-login.html'">Admin Login</button>
    </section>

    <!-- Footer Section -->
    <footer id="contact">
        <p>Contact Us: support@vehicle-services.com | Phone: 123-456-7890</p>
        <p>&copy; 2024 Vehicle Registration & License Services. All rights reserved.</p>
    </footer>
</body>

</html>
