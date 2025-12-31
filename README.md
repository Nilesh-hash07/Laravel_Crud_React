# 1. Clone repository
git clone https://github.com/suresh-ramani/react-crud-app.git
cd react-crud-app

# 2. Backend (Laravel)
composer install --optimize-autoloader --no-dev
cp .env.example .env
php artisan key:generate

# 3. Database configuration (.env)
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=react_crud
DB_USERNAME=root
DB_PASSWORD=

# 4. Run migrations
php artisan migrate

# 5. Frontend (React)
npm install

# 6. Start servers
# Terminal 1 (Backend)
php artisan serve

# Terminal 2 (Frontend)  
npm start
