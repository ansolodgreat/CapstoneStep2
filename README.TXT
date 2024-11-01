# Budget Tracker

Description
💡

The Budget Tracker will be a full-stack web application designed to help users manage their income, expenses, and savings goals. Users can add transactions, categorize them, and generate insights into their spending habits through charts and summaries. The app will also feature recurring expenses, budgeting by category, and saving targets.


Completion

💡

**Estimated Timeframe:** 45-65 hours

The Budget Tracker project has a clear and achievable scope, ensuring it can be completed within the specified 45-65 hour range. Here's a rough breakdown of tasks:

- **User Authentication & Setup:** 8-10 hours
- **Transaction Management (CRUD operations):** 10-12 hours
- **Budget and Category Management:** 8-10 hours
- **Data Visualization (Charts, Reports):** 12-15 hours
- **Recurring Transactions and Reminders:** 5-8 hours
- **Stretch Goals (Mobile Responsiveness, Notifications):** 5-8 hours**Total:** ~55-60 hours


### **Process & Understanding:**

**Goal:**

The goal of the Budget Tracker is to provide users with a straightforward and efficient way to manage their personal finances. It will enable users to track their income and expenses, visualize their spending, and achieve their savings goals.

**Target Demographic:**

- **Users:** Individuals seeking a tool to track their personal or family finances. This includes young adults, professionals, and families aiming to manage monthly expenses, budget for specific goals, and track financial progress.

**Data Source:**

- **Data to Use:** The application will utilize user-inputted data for income, expenses, categories, and savings goals. Users will manually enter their transactions, which will be stored in the app’s database.
- **Data Collection Method:** Transaction details (amount, category, date, description) will be stored via API requests into a backend database. The app will generate reports by querying this data and provide visual feedback to users.

**Database Schema:**

- **Users Table:** User ID, email, password, income
- **Transactions Table:** Transaction ID, user ID, amount, category, date, description
- **Categories Table:** Category ID, name (e.g., groceries, entertainment, rent)
- **Budget Table:** Budget ID, user ID, category, budgeted amount, spent amount
- **Recurring Transactions Table:** Recurring ID, user ID, transaction details, frequency (e.g., monthly)

**API Issues:**

- **Challenge:** Handling large amounts of transaction data over time could impact performance.
- **Solution:** Optimize queries for high-performance and scalability. Potential use of indexing on frequently queried fields (like user ID and date).

**Sensitive Information:**

- **Challenge:** User data, especially regarding personal finances, needs to be securely stored.
- **Solution:** Implement robust encryption (e.g., bcrypt for passwords) and ensure HTTPS for data transmission. Use JWT (JSON Web Tokens) for secure authentication.

### **Functionality:**

**Key Features:**

- **User Authentication:** Secure user login and signup, including password protection and session management.
- **Transaction Management:** Users can add, edit, and delete income and expenses. Each transaction is categorized (e.g., rent, groceries, entertainment) and timestamped.
- **Budgeting by Category:** Users can create budgets for different categories (e.g., spend no more than $500 on groceries per month).
- **Recurring Transactions:** Automate regular expenses (e.g., rent, utilities) and set reminders for when bills are due.
- **Data Visualization:** Display charts and reports of spending habits, such as monthly breakdowns or top categories. Visual feedback will help users understand where they are spending the most.

**User Flow:**

- **User Sign-up/Login:** Users will first create an account or log in with their credentials.
- **Dashboard:** Users will be taken to a dashboard where they can view their current financial overview, including their total income, expenses, and savings progress.
- **Add Transaction:** Users will be able to add transactions by inputting the amount, category, description, and date.
- **View Reports:** Users can view financial reports, such as monthly expenses or spending by category, visualized with charts (using a library like Chart.js).
- **Set Budgets & Savings Goals:** Users will create budgets for specific categories and set financial goals that the app tracks against their actual spending.

### **Stretch Goals:**

- **Mobile Responsiveness:** Ensure the app is fully responsive, allowing users to track their budget from their mobile devices.
- **Push Notifications:** Integrate notifications for bill reminders or budget alerts.
- **CSV Import/Export:** Enable users to upload or download their financial data in CSV format for further analysis.

### **Presentation:**

**Challenges & Solutions:**

- **Real-time Insights:** Calculating large amounts of data, especially for visualizations, can be performance-intensive. To handle this, the app will use pagination and query optimizations for transactions.
- **Security:** Handling sensitive user financial data requires secure practices, such as password hashing (bcrypt), HTTPS for secure communication, and JWT for session management.

**Mentor Guidance:**

- Consider feedback on how to optimize the database schema for efficient querying of large data sets.
- Advice on the feasibility of implementing advanced features like CSV imports and push notifications within the project timeline would be appreciated.

### **Tech Stack:**

- **Frontend:** React, HTML, CSS, JavaScript
- **Backend:** Node.js, Express.js
- **Database:** MongoDB for storing user information, transactions, and budgets
- **Data Visualization:** Chart.js for rendering graphs and charts
- **Authentication:** JWT for token-based authentication, bcrypt for password hashing
- **APIs:** RESTful APIs for handling user requests, transactions, and budgeting features