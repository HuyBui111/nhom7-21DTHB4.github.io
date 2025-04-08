# 🎓 Website Bán Khoá Học Online

> Một nền tảng học trực tuyến giúc người dùng tìm kiếm, đăng ký và học các khoá học chất lượng cao mọi lúc, mọi nơi.

Dự án được xây dựng bằng **ASP.NET Core MVC**, sử dụng **Entity Framework Core** với **Microsoft SQL Server**, giao diện Razor (CSHTML), kết hợp với **CSS** và **JavaScript**.

---

## 🔥 Tính năng nổi bật

### Người dùng (Học viên)
- ✅ Đăng ký / Đăng nhập bằng email
- 📚 Xem danh sách khoá học, tìm kiếm & lọc theo danh mục
- 🛒 Thêm khoá học vào giỏ hàng và thanh toán
- 📂 Xem khoá học đã mua, truy cập nội dung (video, tài liệu)
- 📝 Đánh giá & bình luận khoá học

### Quản trị viên
- 🧑‍💻 Quản lý danh mục, khoá học, người dùng
- 📈 Xem báo cáo doanh thu, thống kê học viên
- ⚙️ Phân quyền người dùng (Admin / Student)
- 📦 Duyệt & cập nhật nội dung khoá học

---

## 🛠️ Công nghệ sử dụng

| Thành phần | Công nghệ |
|------------|-----------|
| Backend    | ASP.NET Core MVC |
| ORM        | Entity Framework Core |
| Database   | Microsoft SQL Server |
| Views      | Razor (CSHTML) |
| Frontend   | HTML, CSS, JavaScript |
| Auth       | ASP.NET Identity |
| Hosting    | IIS / Azure App Service |
| Migration  | `dotnet ef` CLI |
| Container (tuỳ chọn) | Docker |

---

## 📸 Screenshot (Demo UI)
![image](https://github.com/user-attachments/assets/10ed2210-4fe3-4208-8f14-3b9a65d85df0)
![image](https://github.com/user-attachments/assets/b27d19ff-d1c8-4125-8d8d-1f2f71167082)
![image](https://github.com/user-attachments/assets/5c67d1cf-b518-483d-8283-7629c6aabe9e)

---

## ✨ Cài đặt thủ công

### 1. Clone dự án
```bash
git clone https://github.com/HuyBui111/nhom7-21DTHB4.github.io
cd nhom7-21DTHB4.github.io
```

### 2. Cấu hình database
Trong `appsettings.json`, sửa chuỗi kết nối:

```json
"ConnectionStrings": {
  "DefaultConnection": "Server=.;Database=OnlineCourseDb;Trusted_Connection=True;"
}
```

> Hoặc dùng SQL Server Authentication:
```json
"DefaultConnection": "Server=localhost;Database=OnlineCourseDb;User Id=sa;Password=YourPassword123;"
```

### 3. Khởi tạo database
```bash
dotnet ef database update
```

### 4. Chạy ứng dụng
```bash
dotnet run
```

Truy cập website: [http://localhost:5000](http://localhost:5000)

---

## 🐳 Cài đặt bằng Docker (tuỳ chọn)

### Yêu cầu:
- Docker & Docker Compose đã được cài đặt

### 1. Build & chạy
```bash
docker-compose up --build
```

### 2. Truy cập
- Web: http://localhost:5000  
- DB (SQL Server): `localhost:1433` (username: `sa`, password: `YourStrong!Passw0rd`)

---

## 📡 Deploy lên IIS (Windows)

1. Build project:  
   ```bash
   dotnet publish -c Release -o ./publish
   ```

2. Cấu hình IIS:
   - Tạo một website mới trỏ đến thư mục `publish`
   - Gán quyền cho `IIS_IUSRS`
   - Cài đặt `.NET Hosting Bundle` trên máy chủ

---

## ☁️ Deploy lên Azure App Service

1. Tạo App Service + SQL Server trên Azure
2. Cập nhật chuỗi kết nối trong `appsettings.Production.json`
3. Deploy bằng GitHub Actions, Azure DevOps, hoặc Visual Studio

---

## 🥪 Tài khoản thử nghiệm

| Vai trò | Email | Mật khẩu |
|--------|-------|----------|
| Admin  | admin@example.com | Admin@123 |
| User   | user@example.com  | User@123  |

---

## 📁 Cấu trúc thư mục

```
|-- Controllers/
|-- Models/
|-- Views/
|   |-- Shared/
|-- Data/
|-- wwwroot/
|-- Migrations/
|-- appsettings.json
|-- Startup.cs / Program.cs
|-- OnlineCourseApp.csproj
```

---

## 🤝 Đóng góp

Đóng góp được chào đón!

1. Fork repository
2. Tạo nhánh mới: `git checkout -b feature/chuc-nang-moi`
3. Commit thay đổi: `git commit -m "Thêm chức năng X"`
4. Push lên GitHub: `git push origin feature/chuc-nang-moi`
5. Mở Pull Request

---

## 📜 License

Dự án phát hành theo giấy phép [MIT License](LICENSE)

---

> Made with ❤️ by Nhom7WithLuv

