# Logistic Shipping

## Project Overview
Logistic Shipping is a comprehensive application designed to manage and streamline shipping logistics. This project handles order tracking, shipping status updates, and inventory management, ensuring an efficient supply chain process.

## Features
- **Order Management**: Track and manage customer orders seamlessly.
- **Real-time Tracking**: Keep users updated with real-time shipment tracking.
- **Inventory Management**: Monitor and manage inventory effectively.
- **User Authentication**: Secure login and signup functionality.
- **Admin Dashboard**: Manage shipments, view analytics, and update statuses.

## Tech Stack
- **Backend**: Node.js with Express.js
- **Database**: PostgreSQL using Sequelize ORM
- **Frontend**: React with React Router
- **Other Tools**: JWT for authentication, dotenv for configuration management

## Setup Instructions
1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd logistic-shipping
   ```

2. **Install Dependencies**:
   ```bash
   npm install
   ```

3. **Configure Environment Variables**:
   - Create a `.env` file in the root directory.
   - Add the following environment variables:
     ```env
     PORT=2000
     DATABASE_URL=<your_postgresql_connection_string>
     JWT_SECRET=<your_jwt_secret>
     SMTP_HOST=<your_smtp_host>
     SMTP_PORT=<your_smtp_port>
     SMTP_USER=<your_smtp_user>
     SMTP_PASS=<your_smtp_password>
     ```

4. **Set Up the Database**:
   - Run migrations using Sequelize:
     ```bash
     npx sequelize-cli db:migrate
     ```
   - (Optional) Seed the database:
     ```bash
     npx sequelize-cli db:seed:all
     ```

5. **Start the Application**:
   ```bash
   npm start
   ```
   The application will run on `http://localhost:2000` by default.

## API Endpoints
### Public Routes
- **POST** `/auth/login` - User login
- **POST** `/auth/register` - User registration

### Protected Routes
- **GET** `/orders` - Fetch all orders
- **POST** `/orders` - Create a new order
- **GET** `/orders/:id` - Fetch a specific order
- **PUT** `/orders/:id` - Update order details
- **DELETE** `/orders/:id` - Delete an order

### Admin Routes
- **GET** `/admin/dashboard` - View analytics and shipping overview
- **PUT** `/admin/orders/:id/status` - Update shipment status

## Contributing
1. Fork the repository
2. Create a new branch (`git checkout -b feature-branch`)
3. Commit your changes (`git commit -m 'Add new feature'`)
4. Push to the branch (`git push origin feature-branch`)
5. Create a Pull Request

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Contact
For further queries or contributions, contact:
- **Email**: support@logistic-shipping.com
- **GitHub**: [Your GitHub Username](https://github.com/suvm-sharma)
