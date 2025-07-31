# Credit Approval System

This project is a credit approval system that determines loan eligibility based on past loan data. It includes APIs for adding new customers, checking loan eligibility, processing new loans, and viewing loan details.

## Features

- Add a new customer to the customer table
- Check loan eligibility based on credit score
- Process a new loan based on eligibility
- View loan details and customer details
- View all current loan details by customer ID

## Technologies Used

- Django
- PostgreSQL
- Docker
- Docker Compose

## API Endpoints

All APIs run under `/api/v1/`:
1. `/register/`: Add a new customer
2. `/check-eligibility/`: Check loan eligibility based on credit score
3. `/create-loan/`: Process a new loan based on eligibility
4. `/view-loan/loan_id/`: View loan details and customer details by loan ID
5. `/view-loans/customer_id/`: View all current loan details by customer ID

Note: Make sure to add a slash ('/') at the end of the API.

## Pre-requisites

- python
- docker
- Docker Desktop
- docker-compose

## Running the Application

>Clone this project
```bash
git clone https://github.com/Void-786/credit-approvel-system.git
```
>Navigate to the project directory
```bash
cd credit_approval_system
```
>Start the Docker engine by starting the Docker Desktop or by using [OS utilities](https://docs.docker.com/config/daemon/start/)

>Run Docker Compose
```bash
docker-compose up
```
>Access the APIs at
```bash
http://localhost:8000/api/v1/
```

## Adding production secrets
Create a ```.env``` file in the root directory of this project & add a [SECRET_KEY](https://docs.djangoproject.com/en/5.0/ref/settings/#secret-key) for django to use.
>Run the following command in your Django project's Python shell to generate a secret key
```bash
from django.core.management.utils import get_random_secret_key
get_random_secret_key()
```
>Copy the new SECRET_KEY that is generated & paste it to your .env file.
```
SECRET_KEY=your_secret_key_here
```

Note: By default this application uses an insecure key please change it to avoid unwanted attacks.
