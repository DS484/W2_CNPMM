# CRUD Express.js + Sequelize + MySQL

Dự án được tạo sẵn theo slide hướng dẫn. **KHÔNG** bao gồm bài tập MongoDB.

## Yêu cầu
- Node.js >= 18
- MySQL server

## Cấu hình
File `.env` đã được tạo sẵn:
```env
DB_HOST=127.0.0.1
DB_PORT=3306
DB_NAME=crud_db
DB_USER=root
DB_PASS=
```
Sequelize dùng `src/config/config.json` (development) với các thông số tương tự.

## Khởi tạo DB lần đầu
1. Tạo database:
   ```sql
   CREATE DATABASE IF NOT EXISTS crud_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
   ```
2. Cài dependencies và chạy migration:
   ```bash
   npm install
   npx sequelize-cli db:migrate --config src/config/config.json --migrations-path src/migrations --models-path src/models
   ```

## Chạy dự án
```bash
npm run dev
# hoặc
npm start
```
Truy cập: http://localhost:3000

## Các route chính
- `/crud` (form tạo user)
- `/get-crud` (danh sách users)
- `/edit-crud?id=<id>` (form cập nhật)
- `/delete-crud?id=<id>` (xóa user)

---
Tạo: 2025-08-20T01:19:22.599364
