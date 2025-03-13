---
description: Generate sample user data
---

# Faker

Use Case: Simulate user data for testing dashboards, mockups, or reports and is commonly used to quickly generate sample data for prototypes.&#x20;

Coder Breakdown:

* Imports the Faker class from the faker lib to generate random yet realistic fake data. The faker lib contains many functions also called methods that generate random but realistic fake data.&#x20;
* Faker() creates an instance of the Faker class.
* In the below example: Faker() is a class, fake is an object(or instance) of that class. We use this object (fake) to access Faker function like .name(), .email(), etc.&#x20;

```
from faker import Faker

fake = Faker()
print(fake.name())  # Generate fake user name
print(fake.email())  # Generate fake email
```

* Different Faker Data Categories

| **Category**           | **Method Example**          | **Example Output**                     |
| ---------------------- | --------------------------- | -------------------------------------- |
| **Name**               | `fake.name()`               | `John Doe`                             |
| **Email**              | `fake.email()`              | `johndoe@example.com`                  |
| **Phone Number**       | `fake.phone_number()`       | `+1-555-987-6543`                      |
| **Address**            | `fake.address()`            | `123 Fake Street, NY, USA`             |
| **Text**               | `fake.text()`               | `"Lorem ipsum dolor sit amet..."`      |
| **Company**            | `fake.company()`            | `Tech Solutions Ltd.`                  |
| **Job Title**          | `fake.job()`                | `Software Engineer`                    |
| **Date of Birth**      | `fake.date_of_birth()`      | `1985-07-14`                           |
| **Credit Card Number** | `fake.credit_card_number()` | `4539 1234 5678 9012`                  |
| **IP Address**         | `fake.ipv4()`               | `192.168.1.1`                          |
| **UUID**               | `fake.uuid4()`              | `550e8400-e29b-41d4-a716-446655440000` |

* Example usingmultiple Faker methods&#x20;

```
from faker import Faker

fake = Faker()  # Creating an instance/ object of the Faker class

print("Name:", fake.name())  # Generates a fake name
print("Email:", fake.email())  # Generates a fake email
print("Phone:", fake.phone_number())  # Generates a fake phone number
print("Address:", fake.address())  # Generates a fake address
print("Company:", fake.company())  # Generates a fake company name
print("Job Title:", fake.job())  # Generates a fake job title
print("Credit Card:", fake.credit_card_number())  # Generates a fake credit card number
print("IP Address:", fake.ipv4())  # Generates a fake IP address

#To generate it for lets say 10 users, use the following code:
from faker import Faker

fake = Faker()  # Creating an instance of the Faker class

# Generate data for 10 users
for i in range(10):
    print(f"User {i+1}:")
    print("Name:", fake.name())  # Generates a fake name
    print("Email:", fake.email())  # Generates a fake email
    print("Phone:", fake.phone_number())  # Generates a fake phone number
    print("Address:", fake.address())  # Generates a fake address
    print("Company:", fake.company())  # Generates a fake company name
    print("Job Title:", fake.job())  # Generates a fake job title
    print("Credit Card:", fake.credit_card_number())  # Generates a fake credit card number
    print("IP Address:", fake.ipv4())  # Generates a fake IP address
    print("-" * 50)  # Prints a separator line for better readability
```
