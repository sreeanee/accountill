### [accountill.com](https://accountill.com/)
# MERN Stack Invoicing Application
Built with the MERN stack (MongoDB, Express, React and NodeJS).
![Invoice](https://res.cloudinary.com/almpo/image/upload/v1637311386/invoice/invoice-app_tcz0dj.png)


## Update
I am pleased to inform you that the name of this repository has been changed from Arc Invoice to Accountill.
There are so many things coming! Stay tuned!!


Sreetha Aneesh
----

  * [Introduction](#introduction)
  * [Key Features](#key-features)
  * [Technologies used](#technologies-used)
      - [Client](#client)
      - [Server](#server)
      - [Database](#database)
  * [Configuration and Setup](#configuration-and-setup)
  * [Troubleshooting](#troubleshooting)
  * [Maintainer](#maintainer)
  * [License](#license)

## Introduction
This is a project I have been developing and maintaining. A full stack invoicing application made using the MERN stack (MongoDB, Express, React and Nodejs), specially designed for freelancers and small businesses, but can be used for almost any type of business need. With this application, you can send professional invoices, receipts, estimates, quotes, and bills to your clients. You can explore the [Live App](https://accountill.com/) to start sending invoices or download the [Source code](https://github.com/sreetha-aneesh/accountill) to run it on your own server. I am constantly working to improve this project and appreciate any feedback or issue reports.

![Invoice Dashboard](https://res.cloudinary.com/almpo/image/upload/v1637314504/invoice/dashboard_c5z0is.png)

## Key Features
- Send invoices, receipts, estimates, quotations and bills via email
- Generate and send/download pdf invoices, receipts, estimates, quotations and bills via email
- Set due date
- Automatic status change when payment record is added
- Payment history section for each invoice with record about payment date, payment method and extra note
- Record partial payment of invoice
- Clean admin dashboard for displaying all invoice statistics including total amount received, total pending, recent payments, total invoice paid, total unpaid and partially paid invoices
- Multiple user registration
- Authentication using jsonwebtoken (jwt) and Google auth


## Technologies used
This project was created using the following technologies.

#### Client

- React JS
- Redux (for managing and centralizing application state)
- React-router-dom (To handle routing)
- Axios (for making api calls)
- Material UI and CSS Module (for User Interface)
- React simple Snackbar (To display success/error notifications)
- Cloudinary (to allow users to upload their business logo)
- Apex Charts (to display payment history)
- React-google-login (To enable authentication using Google)

#### Server

- Express
- Mongoose
- JWT (For authentication)
- bcryptjs (for data encryption)
- Nodemailer (for sending invoice via email)
- html-pdf (for generating invoice PDFs)

#### Database
MongoDB (MongoDB Atlas)

## Configuration and Setup
In order to run this project locally, simply clone the repository or download as zip and unzip on your machine. 
- Open the project in your preferred code editor.
- Go to terminal -> New terminal (If you are using VS code)
- Split your terminal into two (run the client on one terminal and the server on the other terminal)

In the first terminal
- cd client and create a .env file in the root of your client directory.
- Supply the following credentials

```
REACT_APP_GOOGLE_CLIENT_ID = 
REACT_APP_API = http://localhost:5000
REACT_APP_URL = http://localhost:3000

```

To get your Google ClientID for authentication, go to the credential Page (if you are new, then create a new project first) and follow the following steps:

- Click Create credentials > OAuth client ID.
- Select the Web application type.
- Name your OAuth client and click Create
- Remember to provide your domain and redirect URL so that Google identifies the origin domain to which it can display the consent screen. In development, that is going to be http://localhost:3000 and http://localhost:3000/login
- Copy the Client ID and assign it to the variable REACT_APP_GOOGLE_CLIENT_ID in your .env file

```
$ cd client
$ npm install (to install client-side dependencies)
$ npm start (to start the client)
```
In the second terminal
- cd server and create a .env file in the root of your server directory.
- Supply the following credentials

```
DB_URL = 
PORT = 5000
SECRET = 
SMTP_HOST = 
SMTP_PORT = 
SMTP_USER = 
SMTP_PASS = 

```

Please follow standard documentation to create your mongoDB connection url, which you will use as your DB_URL.

```
$ cd server
$ npm install (to install server-side dependencies)
$ npm start (to start the server)
```

## Troubleshooting
If you are getting an error while trying to send or download PDF, please run the following in your server terminal:

```
$ npm install html-pdf -g
$ npm link html-pdf
$ npm link phantomjs-prebuilt
```

## Docker

Using docker is simple. Just add the .env contextualized with the docker network.

e.g:

> goes to path "server/.env"
```
DB_URL = mongodb://mongo:27017/arch
PORT = 5000
SECRET = 
SMTP_HOST = 
SMTP_PORT = 
SMTP_USER = 
SMTP_PASS = 
```
> goes to path "client/.env"
```
REACT_APP_GOOGLE_CLIENT_ID = 
REACT_APP_API = http://localhost:5000
REACT_APP_URL = http://localhost
```

And run

```
docker-compose -f docker-compose.prod.yml build

And then

docker-compose -f docker-compose.prod.yml up
```

## Comment
I intend to keep adding more features to this application. If you find this project useful, please consider giving it a star to support further development and improvements.


## Maintainer

- LinkedIn: [Sreetha Aneesh](https://www.linkedin.com/in/sreetha-aneesh-47a96130/)
- Email: [sreeanee2021@gmail.com](mailto:sreeanee2021@gmail.com)
- GitHub: [sreetha-aneesh](https://github.com/sreetha-aneesh)

## License

- This project is [MIT](https://github.com/sreetha-aneesh/accountill/blob/master/LICENSE.md) licensed. Original work by Panshak.

## About the Developer
Sreetha Aneesh is a Senior Full Stack Developer with over 5 years of experience in full-stack application development, backend engineering, and enterprise software delivery. Skilled in Java, Spring Boot, React.js, and cloud technologies, she focuses on building scalable, high-performance applications and contributing to robust software solutions across diverse technical environments.