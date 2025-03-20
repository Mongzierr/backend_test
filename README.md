


การติดตั้งและรันโปรเจค

1. Clone โปรเจค
ทำการ clone โปรเจคจาก GitHub ไปยังเครื่องของคุณ

```bash
git clone https://github.com/Mongzierr/backend_test_trai.git
```
2. ติดตั้ง Dependencies
```bash
npm install
```
3. สร้างไฟล์ .env
   
   ```ini
   DATABASE_URL="postgresql://<username>:<password>@<host>:5432/<DBname>?schema=public"
   ```

   Example: run at localhost:5432
   ```ini
   DATABASE_URL="postgresql://postgres:1234@localhost:5432/test?schema=public"
   ```
4. การตั้งค่าฐานข้อมูล
ให้สร้างฐานข้อมูล PostgreSQL และใช้ Prisma สำหรับการตั้งค่า Schema และ Migrations

```bash
npx prisma migrate dev // ถ้าไม่ได้ให้ใช้ sudo npx
```


5. รัน Seed ข้อมูล
```bash
npm run seed
```

6. ตรวจสอบข้อมูล
```bash
npx prisma studio
```

7. การรันโปรเจค
หลังจากที่ติดตั้งทุกอย่างเรียบร้อยแล้ว คุณสามารถรันโปรเจคโดยใช้คำสั่ง
```bash
npm start
```

8. ทดสอบ api ด้วย postman โดยจะอยู่ในไฟล์ apitest.postman.json สามารถ import เข้า postman ได้เลย

9. ทดสอบ api users/register
    
   req: ```bash
   {
    "username": "johnsnoop",
  "email": "test02@example.com",
  "phone_number": "0123456789",
  "password": "abcdefghgffdgdfg"
}```
   
