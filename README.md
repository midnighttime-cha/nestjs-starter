# เริ่มต้นใช้งาน NestJS ติดตั้ง Nest CLI 
![Nestjs Website](https://storage.kaikannook.com/image/showimage/common/blog/6204ab0f546247d9cc24b4e2f516528d.png)

พื้นฐานความรู้เบื้องต้น
- node.js, npm/yarn
- RESTful API
- javacript/TypeScript

## ติดตั้ง Nest CLI
```bash
yarn add global @nestjs/cli
```
หรือ

```bash
yarn add global @nestjs/cli
```
เมื่อติดตั้งเรียบร้อยแล้วสามารถทดสอบโดย
```bash
nest -v
```

## สร้าง Project
```bash
nest new [project-name]
cd [project-name]
yarn install
```
ทดสอบการทำงาน
```bash
yarn start
```
กรณีต้องการแสดง log ของระบบให้ใช้
```bash
yarn start:dev
```
เปิด URL: (http://localhost:3000/)
ถ้าระบบปรากฏตามรูปต่อไปนี้

![server init](https://storage.kaikannook.com/image/showimage/common/blog/10105b953eda9ecc107ebc106e452dfed43c.png)

## เริ่มต้นกันที่ไฟล์ `main.ts` กันเลย
ติดตั้ง Platform ระหว่าง `platform-express` กับ `platform-fastify` สำหรับผมขอเลือกใช้งาน `platform-express`
```bash
yarn add @nestjs/platform-express
```
จากนั้นใส่ code ต่อไปนี้แทนที่
```javascript
...
const app = await NestFactory.create(AppModule);
...
```
แทนที่ด้วย
```javascript
...
const app = await NestFactory.create<NestExpressApplication>(AppModule);
...
```
ทำการ import `NestExpressApplication` ตามรูป

![Import NestExpressApplication](https://storage.kaikannook.com/image/showimage/common/blog/f6b5be51018c7ccf54a938bd410107c3662.png)




















