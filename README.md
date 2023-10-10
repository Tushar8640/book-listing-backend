# Book Catalog Server

**A Robust Backend Service for Managing Your Book Catalog with Authentication and Authorization**

Ripository Link: https://github.com/Tushar8640/book-listing-backend
Server Link: https://assignment-8-sooty.vercel.app/

## Tech Stack:

- **Server**: Node.js, Express.js
- **Database and ORM**: PostgreSQL (Supabase), Prisma
- **Type Safety and Validation**: TypeScript, Zod
- **Authentication and Authorization**: JSON Web Token, Bcrypt
- **Linters and Formatters**: ESLint, Prettier
- **Pre-commit Hooks**: Husky, Lint Staged

## Highlighted Features:

- **User Authentication and Authorization**: Secure your application with user-specific access controls.
- **Admin and User Distinction**: Differentiate between admin and user roles for enhanced security and functionality.
- **Book Management**: Create, search, filter, sort, and paginate your book catalog effortlessly.
- **Order Processing**: Streamline order creation and access your own orders efficiently.

## Getting Started:

1. Clone the repository:

   ```bash
   git clone https://github.com/mohammad-naimur-rahman/book-catalog-service
   ```

2. Install the dependencies:

   ```bash
   yarn
   ```

3. Configure environment variables (Refer to `.env.example`).

4. Migrate the database:

   ```bash
   yarn migrate
   ```

5. Run locally at `http://localhost:PORT`:

   ```bash
   yarn dev
   ```

6. Build the application:

   ```bash
   yarn build
   ```

Get started with your Book Catalog Service today and experience a seamless and secure book management system!


## Available API endpoints:

### Authentication

**Signup User**

POST - https://assignment-8-sooty.vercel.app/api/v1/auth/signup

**Login User**

POST - https://assignment-8-sooty.vercel.app/api/v1/auth/signin

**_For Admin access: Login with this credentials:_**

```json
  {
    "email" "naimur@gmail.com",
    "password: "iamnaeem"
  }
```

### Users

**Get all users**

GET - https://assignment-8-sooty.vercel.app/api/v1/users

(Need admin bearer token)
Example: `Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiJkNWEzNTNlNy04NTY5LTQ3MTUtYTZmMS01MzdhYjJhYWY1NmQiLCJyb2xlIjoiYWRtaW4iLCJpYXQiOjE2OTY5NDQyMTYsImV4cCI6MTY5NzAzMDYxNn0.HQ1pZ8VDF2vJa-aQIww3K_NlKqNcM0OaStSoSACSDSw`

**Get a single user**

GET - https://assignment-8-sooty.vercel.app/api/v1/users/0ceb5991-8eae-4706-8988-2f27d9252907

(Need admin bearer token)

**Update User**

PATCH - https://assignment-8-sooty.vercel.app/api/v1/users/0ceb5991-8eae-4706-8988-2f27d9252907

(Need admin bearer token)

**Delete User**

DELETE - https://assignment-8-sooty.vercel.app/api/v1/users/0ceb5991-8eae-4706-8988-2f27d9252907

(Need admin bearer token)

**Get User Own Profile**

GET - https://assignment-8-sooty.vercel.app/api/v1/users/profile

(Need bearer token)

**Make a user admin**

PATCH - https://assignment-8-sooty.vercel.app/api/v1/users/make-admin/0ceb5991-8eae-4706-8988-2f27d9252907

(Need admin bearer token)

### Categories

**Create Category**

POST - https://assignment-8-sooty.vercel.app/api/v1/categories/create-category

(Need admin bearer token)

**Get All Categories**

GET - https://assignment-8-sooty.vercel.app/api/v1/categories

**Get Single Category**

GET - https://assignment-8-sooty.vercel.app/api/v1/categories/ce9b5ba7-3b82-47cf-a143-a86f93920195

**Update Category**

PATCH - https://assignment-8-sooty.vercel.app/api/v1/categories/ce9b5ba7-3b82-47cf-a143-a86f93920195

(Need admin bearer token)

**Delete Category**

https://assignment-8-sooty.vercel.app/api/v1/categories/ce9b5ba7-3b82-47cf-a143-a86f93920195

(Need admin bearer token)

### Books

**Get all books**

GET - https://assignment-8-sooty.vercel.app/api/v1/books

PARAMS EXAMPLE
| params | Value |
|-------------|-------------------|
| page | 1 |
| size | 10 |
| sortBy | price |
| sortOrder | desc |
| search | J.D. Salinger |
| category | e32faaf6-c2bf-4361-9b20-622f2b87da25 |
| minPrice | 9.9 |
| maxPrice | 49.9 |

**Create book**

POST - https://assignment-8-sooty.vercel.app/api/v1/books/create-book

(Need admin bearer token)

**Get a single book**
GET - https://assignment-8-sooty.vercel.app/api/v1/books/57a2ef28-b887-4f63-be6a-874f0c81b7a7

**Get a book by category**
https://assignment-8-sooty.vercel.app/api/v1/books/ce9b5ba7-3b82-47cf-a143-a86f93920195/category

**Update book**

PATCH - https://assignment-8-sooty.vercel.app/api/v1/books/57a2ef28-b887-4f63-be6a-874f0c81b7a7

(Need admin bearer token)

**Delete a book**

DELETE - https://assignment-8-sooty.vercel.app/api/v1/books/57a2ef28-b887-4f63-be6a-874f0c81b7a7

(Need admin bearer token)

### Order

**Place Order**

POST - https://assignment-8-sooty.vercel.app/api/v1/orders/create-order

(Need bearer token)

**GEt single order**

GET - https://assignment-8-sooty.vercel.app/api/v1/orders/661027a6-8fd2-4b11-8207-4db9134c9aa3

(Admin needs his bearer token, and user needs his own bearer token)

**Get all orders**

GET - https://assignment-8-sooty.vercel.app/api/v1/orders/

(Need admin bearer token)

Thanks for visiting this project!
