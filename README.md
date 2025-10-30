## UBIKZ- FASHION ECOMMERCE🐦‍🔥

Ubikz is a fast fashion brand website that offers fast fashion products designed using modern web technologies following a REST architecture that allows scalability and high end performance across thousands of users.

📲*Deployed on- https://ubikz-fashion-ecommerce.onrender.com*

![HomePage](./visuals/homepage-head.png)

## General Features

- Wide Categorization of products available across website
- Integrated Payments Gateway with Stripe
- Detailed Product pages with information such as descriptions, Product Images Slider and Size Guide
- Comments and reviews are added for users to interact with each other. Also replies are allowed on comments allowing users to reply to comments.
- Secure Login/SignUp functionality is added allowing users to signup/login & logout easily from the website
- The STMP Mail system alert users with welcomes, password resets information and other website alerts
- Ubikz follows a modern genZ fashion theme and similar styling to Indian Fast Fashion Brand Bewakoof following a modern color scheme and vibrance
- The website contains an account panel wherein users can review the orders placed on the website
- The comprehensive admin panel allows for the admin/management to add products easily through a comprehensive panel that allows for easy creation/deletion and updating the listed products on the website.
- With ubikz the goal was to practice modern ecommerce platform building with advanced webhook based payment gateways and Client Server REST Design using various functionalities such as advanced filtering/sorting/pagination/limiting of products and comprehensive user management using RBA'S/Hashing and many other modern techniques. The authentication module although build back in 2023 is still very comprehensive and reliant for small-medium scale applications along with SMTP Mail integration. The website was overall very helpful for me to learn building complex ecommerce platforms such as Ananya Sales & DM Sales that are a very polished work on the UBIKZ Starter frame.

The following Readme will guide you further with the project generalized documentation and workflow along with project visuals.

### Architecture Overview
The UBIKZ-fashion-ecommerce repository is a Node.js powered fast fashion brand website that leverages modern web technologies and follows a REST architecture. The architecture is designed to ensure scalability and high performance across thousands of users. The primary languages used are JavaScript,HTML,CSS,PUG TEMPLATE ENGINE and modern Node JS framework & modules. A complete log of all developer dependencies and modules used can be found in package-lock.json file attached to the repo. I would now continue by discussion individual features-

#### 1. HomePage Design
![Homepage complete](./visuals/homepage-layout.png)
*The above homepage design was inspired from Bewakoof fast fashion ecommerce website representing a modern, clean, genz- aesthetic layout that is both minimal and easy to navigate for all users*

#### 2. Authentication
*The project follows a robust,simple,modern and effective easy to integrate authentication system goverened by my custom authController.js file built completely from scratch using modules such as bcrypt for encryption and security. This system was most popular back in 2024 when i built this website from scratch. The complete authentication system can be reviewed by accessing the authController.js file. It allows users for easy login,signup and even password resets using Nodemailer and Brevo SMTP system. It uses the basic JWT Authentication system wherein a token is issued and valid until expiry. In my later projectssuch as DM Sales i have implemented Access Refresh token system which is considered modern and better performant for 2025 standards.*
- Signup
  
  ![Signup](./visuals/signup.png)
- Login
  
  ![Login](./visuals/login.png)
- Login Navigation
  
  ![Login Header](./visuals/login-header.png)
- Forgot Password
  
  ![Forget Password](./visuals/forgot-password.png)

#### Product Filtering & Aggregation
*Through UBIKZ i have triend to implement a simple yet efficient Node JS 18 standard filtering,sorting,paginating & limiting system that allows both users and admin team to categorize products for easy access and functionality also i have attached an aggregation process that allows to extract top 5 products using the MONGO DB AGGREGATION pipeline also category wise stats. The code can be accessed from within the UTILS folder with the APIFeatures class that is a JS class based implementation to easily implement the operations using custom object flow*

- Main Category Menu

  ![Filtering](./visuals/menu-categories.png)
- Mens Category Page
  
  ![Category Page Men](./visuals/men-category-page.png)
- Sub Category Page
  
  ![Category Page Men](./visuals/subcategory-bottom-wear.png)

#### USER ACCOUNT
*The User system allows for users to easily access the account page,cart and orders section allowing for a robust user interface and design*
- Account Page
  
  ![Account Page](./visuals/account.png)
- Cart Page

  ![Cart Page](./visuals/cart.png)
- User Payments
  *The website payments are managed by the integrated stripe module that allows for international and national payments leading to a polished user eperience currently in test mode*

  ![Cart Page](./visuals/stripe-payments.png)
  
#### ADMIN PANEL 
*UBIKZ offers a simple yet efficient admin panel that boasts of design simplicity and functionality while google analytics provide the basic analytical data this panel is focused on on site opertions suach as adding/removing products etc...*
- ADMIN PAGE

  ![Admin Page](./visuals/admin.png)
- Admin Add Product

  ![Admin Add Product](./visuals/admin-add-products.png)
- Admin Update product
  
  ![Admin Update Product](./visuals/admin-update-products.png)
### Setup & Installation
To set up and install the UBIKZ-fashion-ecommerce project, follow these steps:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/UBIKZ-fashion-ecommerce.git
   cd UBIKZ-fashion-ecommerce
   ```

2. **Install Dependencies:**
   ```bash
   npm install
   ```

3. **Start the Development Server:**
   ```bash
   npm start
   ```

### API Documentation
The API documentation provides details on the endpoints and their functionalities. The following are the key API routes:

- **Order Routes:**
  - `GET /api/orders`: Retrieve a list of orders.
  - `POST /api/orders`: Create a new order.
  - `GET /api/orders/:id`: Retrieve a specific order by ID.
  - `PUT /api/orders/:id`: Update a specific order by ID.
  - `DELETE /api/orders/:id`: Delete a specific order by ID.

- **Overview Routes:**
  - `GET /api/overview`: Retrieve overview data.

- **Product Routes:**
  - `GET /api/products`: Retrieve a list of products.
  - `POST /api/products`: Create a new product.
  - `GET /api/products/:id`: Retrieve a specific product by ID.
  - `PUT /api/products/:id`: Update a specific product by ID.
  - `DELETE /api/products/:id`: Delete a specific product by ID.

- **Review Routes:**
  - `GET /api/reviews`: Retrieve a list of reviews.
  - `POST /api/reviews`: Create a new review.
  - `GET /api/reviews/:id`: Retrieve a specific review by ID.
  - `PUT /api/reviews/:id`: Update a specific review by ID.
  - `DELETE /api/reviews/:id`: Delete a specific review by ID.

- **Sale Routes:**
  - `GET /api/sales`: Retrieve a list of sales.
  - `POST /api/sales`: Create a new sale.
  - `GET /api/sales/:id`: Retrieve a specific sale by ID.
  - `PUT /api/sales/:id`: Update a specific sale by ID.
  - `DELETE /api/sales/:id`: Delete a specific sale by ID.

- **User Routes:**
  - `GET /api/users`: Retrieve a list of users.
  - `POST /api/users`: Create a new user.
  - `GET /api/users/:id`: Retrieve a specific user by ID.
  - `PUT /api/users/:id`: Update a specific user by ID.
  - `DELETE /api/users/:id`: Delete a specific user by ID.

- **View Routes:**
  - `GET /api/views`: Retrieve a list of views.

### Configuration
Configuration settings are typically stored in environment variables or configuration files. The project uses a `.env` file to manage environment-specific settings. Example configuration settings include:

- `DB_HOST`: Database host.
- `DB_USER`: Database user.
- `DB_PASSWORD`: Database password.
- `DB_NAME`: Database name.
- `JWT_SECRET`: Secret key for JSON Web Tokens.
- `STRIPE_API_KEY`: Stripe API key for payment processing.
- Many more PROCESS ENV VARIABLES ARE UTILIZED THROUGHOUT THE PROJECT CODE...

### Deployment Instructions
To deploy the UBIKZ-fashion-ecommerce project, follow these steps:

1. **Build the Project:**
   ```bash
   npm run build
   ```

2. **Deploy to a Server:**
   - Use a hosting service like Heroku, AWS, or DigitalOcean.
   - Configure the server to run the Node.js application.

3. **Database Migration:**
   - Ensure the database schema is up-to-date.
   - Run database migrations if necessary.

4. **Environment Configuration:**
   - Set up environment variables on the server.
   - Configure the server to use the correct database and API keys.

5. **Monitoring and Logging:**
   - Set up monitoring and logging to track application performance and errors.
   - Use tools like New Relic or ELK Stack for monitoring and logging.

By following these guidelines, you can effectively set up, develop, and deploy the UBIKZ-fashion-ecommerce project.
