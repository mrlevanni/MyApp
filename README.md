# Solar Quote App

Ứng dụng tư vấn báo giá lắp đặt hệ thống điện năng lượng mặt trời tại Việt Nam.

## ✨ Tính năng

- 📝 **Form nhập thông tin khách hàng**: Tên, tiền điện hàng tháng, % tiết kiệm mong muốn, phân bổ sử dụng điện
- 🧮 **Tính toán tự động**: Hệ thống tự động tính toán công suất cần thiết và chọn thiết bị phù hợp
- 🔧 **Tùy chỉnh báo giá**: Có thể thay đổi loại tấm pin, pin lưu trữ, inverter và số lượng
- 📊 **Báo giá chi tiết**: Hiển thị đầy đủ thông tin sản phẩm, giá cả, bảo hành
- 📄 **Xuất PDF**: Tạo file PDF báo giá chuyên nghiệp có logo và thông tin công ty
- 💾 **Database linh hoạt**: Sử dụng Excel làm database, có thể upload file Excel mới
- 🌐 **Giao diện đẹp**: Responsive design với Bootstrap 5

## 🏗️ Kiến trúc

- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **Backend**: Node.js + Express
- **Database**: Excel (.xlsx) files
- **PDF Generation**: Puppeteer
- **Deployment**: Cloudflare Pages

## 📦 Cài đặt

### 1. Clone và cài đặt dependencies

\`\`\`bash
git clone <repository-url>
cd solar-quote-app
npm install
\`\`\`

### 2. Chạy ứng dụng

#### Development mode
\`\`\`bash
npm run dev
\`\`\`

#### Production mode
\`\`\`bash
npm start
\`\`\`

Ứng dụng sẽ chạy tại: http://localhost:3000

### 3. Build cho Cloudflare Pages

\`\`\`bash
npm run build
\`\`\`

## 📊 Database Excel

File \`data/solar_database.xlsx\` chứa 4 sheet:

1. **PV_Panels**: Thông tin tấm pin mặt trời
2. **Batteries**: Thông tin pin lưu trữ
3. **Inverters**: Thông tin inverter
4. **Accessories**: Phụ kiện và chi phí lắp đặt

### Cấu trúc dữ liệu:

#### PV_Panels
| Mã PV | Tên sản phẩm | Công suất (W) | Giá (VND) | Thương hiệu | Bảo hành (năm) |

#### Batteries
| Mã Pin | Tên sản phẩm | Dung lượng (kWh) | Giá (VND) | Thương hiệu | Bảo hành (năm) |

#### Inverters
| Mã Inverter | Tên sản phẩm | Công suất (kW) | Giá (VND) | Thương hiệu | Bảo hành (năm) |

#### Accessories
| Mã phụ kiện | Tên sản phẩm | Đơn vị | Giá (VND) | Ghi chú |

## 🚀 Deployment trên Cloudflare Pages

### 1. Push code lên GitHub

### 2. Kết nối Cloudflare Pages với GitHub repository

### 3. Cấu hình build:
- **Build command**: \`npm run build\`
- **Build output directory**: \`public\`

### 4. Environment variables (nếu cần):
- \`NODE_ENV=production\`

## 🔧 API Endpoints

- \`GET /\` - Trang chủ
- \`GET /api/equipment\` - Lấy danh sách thiết bị
- \`POST /api/calculate-quote\` - Tính toán báo giá
- \`POST /api/customize-quote\` - Tùy chỉnh báo giá
- \`POST /api/upload-database\` - Upload file Excel database
- \`POST /api/generate-pdf\` - Tạo file PDF báo giá

## 💡 Cách sử dụng

### 1. Nhập thông tin khách hàng
- Tên khách hàng
- Số tiền điện hàng tháng (VND)
- Mức tiết kiệm mong muốn (%)
- Phân bổ sử dụng điện buổi sáng/tối (%)

### 2. Xem báo giá tự động
- Hệ thống sẽ tính toán và đề xuất cấu hình phù hợp
- Hiển thị chi tiết sản phẩm, giá cả, tiết kiệm dự kiến

### 3. Tùy chỉnh (nếu cần)
- Thay đổi loại tấm pin, pin lưu trữ, inverter
- Điều chỉnh số lượng theo nhu cầu
- Tính lại báo giá tự động

### 4. Xuất PDF
- Upload logo công ty (tuỳ chọn)
- Nhập tên công ty và slogan
- Tải xuống file PDF báo giá chuyên nghiệp

## 🔄 Cập nhật Database

### Qua giao diện web:
1. Vào trang admin (nếu có)
2. Upload file Excel mới theo đúng format

### Thay thế trực tiếp:
1. Thay thế file \`data/solar_database.xlsx\`
2. Restart ứng dụng

## 🎨 Customization

### Thay đổi theme màu sắc:
Chỉnh sửa CSS variables trong \`public/index.html\`:

\`\`\`css
:root {
    --primary-color: #f39c12;    /* Màu chính */
    --secondary-color: #27ae60;  /* Màu phụ */
    --dark-color: #2c3e50;       /* Màu tối */
}
\`\`\`

### Thêm/sửa logic tính toán:
Chỉnh sửa file \`src/utils/calculator.js\`

### Tùy chỉnh template PDF:
Chỉnh sửa file \`src/utils/pdfGenerator.js\`

## 📝 License

MIT License - Xem file LICENSE để biết thêm chi tiết.

## 🤝 Contributing

1. Fork the project
2. Create your feature branch (\`git checkout -b feature/AmazingFeature\`)
3. Commit your changes (\`git commit -m 'Add some AmazingFeature'\`)
4. Push to the branch (\`git push origin feature/AmazingFeature\`)
5. Open a Pull Request

## 📞 Support

Nếu bạn gặp vấn đề hoặc có câu hỏi, vui lòng tạo issue trên GitHub repository.

---

Made with ❤️ for Solar Energy Industry in Vietnam