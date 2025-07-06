# mailUsingCache

📧 Spring Boot Email Sender with Manual Caching
This is a beginner-friendly Spring Boot application that allows you to send emails to users and cache them manually using in-memory storage.

✅ Features
Send emails using Gmail SMTP

Store user info (name & email)

Manually cache sent users using HashMap

Retrieve cached users

Schedule daily email reminders

REST APIs tested with Postman

🛠 Technologies Used
Java 17+

Spring Boot

Spring Web

Spring Data JPA (with optional MySQL)

JavaMailSender

Manual in-memory caching (no Redis/ehcache)

📦 Project Structure
bash
Copy
Edit
com.example
├── controller      # MailController
├── entity          # UserInfo entity
├── repository      # MailRepo (JPA)
├── service         # MailService + MailImpl
├── scheduler       # MailScheduler
└── EmailSenderApplication.java
🚀 How to Run
Clone the repo:

bash
Copy
Edit
git clone https://github.com/your-username/email-sender-app.git
cd email-sender-app
Configure your application.properties:

ini
Copy
Edit
spring.mail.username=your_email@gmail.com
spring.mail.password=your_app_password
spring.datasource.url=jdbc:mysql://localhost:3306/yourdb
Run the app:

bash
Copy
Edit
./mvnw spring-boot:run
🔁 API Endpoints
➤ POST /mail/send
Send email and cache user
Body:

json
Copy
Edit
{
  "name": "xyz",
  "email": "xyz@example.com"
}
➤ GET /mail/users
Fetch all cached users

📝 License
This project is open source and available under the MIT License.

