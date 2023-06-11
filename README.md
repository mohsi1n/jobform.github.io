<!DOCTYPE html>
<html>
<head>
    <title>Job Provider Registration</title>
    <script>
        function redirectToWhatsApp() {
            var name = document.getElementById("name").value;
            var phone = document.getElementById("phone").value;
            var age = document.getElementById("age").value;
            
            var message = "Hello, I am interested in job opportunities. My details are: \n\nName: " + name + "\nPhone: " + phone + "\nAge: " + age;
            var encodedMessage = encodeURIComponent(message);
            var whatsappLink = "https://api.whatsapp.com/send?phone=923231426352&text=" + encodedMessage;
            
            window.location.href = whatsappLink;
        }
    </script>
</head>
<body>
    <h1>Job Provider Registration</h1>
    <form>
        <label for="name">Name:</label>
        <input type="text" id="name" required><br><br>
        
        <label for="email">Gmail:</label>
        <input type="email" id="email" required><br><br>
        
        <label for="phone">Phone Number:</label>
        <input type="tel" id="phone" required><br><br>
        
        <label for="age">Age:</label>
        <input type="number" id="age" required><br><br>
        
        <input type="button" value="Register" onclick="redirectToWhatsApp()">
    </form>
</body>
</html>
