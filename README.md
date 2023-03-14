# Install Tailwind

1. สร้าง nodejs project จากนั้นเข้าไปที project แล้วใช้คำสั่ง `npm init`
2. เปิด install tailwind ด้วยคำสั่ง `npm install -D tailwindcss`
3. สร้าง file ใช้จัดการการตั้งค่าของ tailwind ด้วยคำสั่ง `npx tailwindcss init` จะได้ file ที่ชื่อว่า `tailwind.config.js`
4. จากนั้นตั้งค่า file `tailwind.config.js` ตามนี้

```javascript
module.exports = {
  content: ["*.{html,js}", "./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

5. สร้าง folder `src` และ `public` ด้าน `src` ในสร้าง file ชื่อว่า `style.css` เข้าไปที่ `src/style.css` แล้วพิมพ์ code ตามนี้

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

6. เพิ่ม script ที่ file `package.json` เพื่อทำการสร้าง `css` ที่ใช้จริงของ project นี้
7. สร้าง file `index.html` แล้วพิมพ์ code ตามนี้

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tailwind CSS</title>
    <link rel="stylesheet" href="./public/style.css" />
  </head>

  <body>
    <div
      class="flex justify-center items-center w-screen h-screen text-green-600"
    >
      Center Text
    </div>
  </body>
</html>
```

8. เปิด command line และพิมพ์คำสั่ง `npm run build` หรือ `yarn build` จะได้ file `public/style.css`
