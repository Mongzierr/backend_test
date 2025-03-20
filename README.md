


การติดตั้งและรันโปรเจค

1. Clone โปรเจค
ทำการ clone โปรเจคจาก GitHub ไปยังเครื่องของคุณ

```bash
git clone https://github.com/yourusername/test-crypto.git
cd test-crypto
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
5. การรันโปรเจค
หลังจากที่ติดตั้งทุกอย่างเรียบร้อยแล้ว คุณสามารถรันโปรเจคโดยใช้คำสั่ง
```bash
npm start
```

6. รัน Seed ข้อมูล
```bash
npm run seed
```

7. ตรวจสอบข้อมูล
```bash
npx prisma studio
```
