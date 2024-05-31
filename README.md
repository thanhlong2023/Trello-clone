"scripts": {
"dev": "vite --host",
"build": "vite build --base=./",
"lint": "eslint . --ext js,jsx --report-unused-disable-directives --max-warnings 0",
"preview": "vite preview"
},

- "dev": "vite --host",
  VITE v5.2.12 ready in 790 ms

➜ Local: http://localhost:5173/
➜ Network: http://172.19.32.1:5173/
➜ Network: http://192.168.1.9:5173/
➜ Network: http://192.168.137.1:5173/
➜ press h + enter to show help

- "build": "vite build --base=./",

buidl folder dist, đẩy dự án lên production
thêm ./ trước đường dẫn path

- "lint": "eslint . --ext js,jsx --report-unused-disable-directives --max-warnings 0",
  sytax code error

- "preview": "vite preview"
  nhảy vào dist check trước khi đẩy lên production
  preview production

luồng code từ main.jsx => id: root (index.html) => render: App
