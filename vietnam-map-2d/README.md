# 🗺️ Bản đồ 2D Việt Nam – ArcGIS JavaScript API

Bài tập thực hành nhóm – **Loại 1: Bản đồ 2D** sử dụng ArcGIS Maps SDK for JavaScript.

## 📋 Mô tả

Ứng dụng bản đồ web hiển thị bản đồ 2D Việt Nam với đầy đủ 3 loại đối tượng địa lý:

| Loại đối tượng | Số lượng | Mô tả |
|---|---|---|
| 🔴 **Đa giác** (Polygon) | **7** | Các tỉnh/thành phố lớn của Việt Nam |
| 🔵 **Đường** (Polyline) | **7** | Các con sông và quốc lộ quan trọng |
| 📍 **Điểm** (Point) | **10** | Các địa danh và di sản du lịch nổi tiếng |

## ✅ Đáp ứng yêu cầu bài tập

### Yêu cầu đã hoàn thành:

- ✅ **Có ít nhất n đa giác, n đường và n điểm** – đủ cho nhóm tối đa 7 người
- ✅ **Hiển thị thông tin khi click** – popup chi tiết với bảng thông tin + mô tả cho mọi đối tượng
- ✅ **Điểm dùng picture marker** – SVG icon hình pin với emoji đặc trưng cho từng địa điểm
- ✅ **Màu sắc khác nhau** – mỗi tỉnh/đường/điểm có màu riêng biệt

## 🏙️ Danh sách đối tượng

### Đa giác – Tỉnh/Thành phố

| # | Tên | Màu |
|---|---|---|
| 1 | Hà Nội | Đỏ `#e74c3c` |
| 2 | TP. Hồ Chí Minh | Cam `#e67e22` |
| 3 | Đà Nẵng | Xanh lá `#27ae60` |
| 4 | Thừa Thiên Huế | Tím `#8e44ad` |
| 5 | Cần Thơ | Xanh dương `#2980b9` |
| 6 | Hải Phòng | Ngọc `#16a085` |
| 7 | Khánh Hòa (Nha Trang) | Cam đậm `#d35400` |

### Đường – Sông & Quốc lộ

| # | Tên | Loại | Style |
|---|---|---|---|
| 1 | Sông Hồng | Sông lớn | Liền nét |
| 2 | Sông Mê Kông (Cửu Long) | Sông quốc tế | Liền nét |
| 3 | Quốc lộ 1A | Quốc lộ xuyên Việt | Nét đứt |
| 4 | Sông Đà | Phụ lưu sông Hồng | Liền nét |
| 5 | Đường Hồ Chí Minh | Quốc lộ / Di tích | Nét chấm |
| 6 | Sông Thu Bồn | Sông địa phương | Liền nét |
| 7 | Quốc lộ 14 – Tây Nguyên | Quốc lộ | Nét đứt ngắn |

### Điểm – Địa danh & Du lịch

| # | Tên | Icon | Di sản |
|---|---|---|---|
| 1 | Hồ Hoàn Kiếm | 🏛️ | Di tích quốc gia đặc biệt |
| 2 | Vịnh Hạ Long | 🏝️ | Di sản Thiên nhiên UNESCO |
| 3 | Phố cổ Hội An | 🏮 | Di sản Văn hóa UNESCO (1999) |
| 4 | Cố đô Huế | 👑 | Di sản Văn hóa UNESCO (1993) |
| 5 | Thánh địa Mỹ Sơn | 🗿 | Di sản Văn hóa UNESCO (1999) |
| 6 | Phong Nha – Kẻ Bàng | 🦎 | Di sản Thiên nhiên UNESCO (2003) |
| 7 | Fansipan – Sa Pa | ⛰️ | Nóc nhà Đông Dương 3.143m |
| 8 | Dinh Độc Lập | 🏛️ | Di tích lịch sử 30/4/1975 |
| 9 | Chợ nổi Cái Răng | 🚢 | Di sản văn hóa phi vật thể |
| 10 | Mũi Cà Mau | 🌊 | Điểm cực Nam Việt Nam |

## 🚀 Cách chạy

Chỉ cần mở file `index.html` trong trình duyệt web hiện đại (Chrome, Firefox, Edge):

```bash
# Dùng Python HTTP server (tùy chọn)
python -m http.server 8080

# Hoặc mở thẳng file
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

> **Lưu ý:** Ứng dụng cần kết nối internet để tải ArcGIS SDK từ CDN (`js.arcgis.com`).

## 🛠️ Công nghệ sử dụng

- **ArcGIS Maps SDK for JavaScript** v4.29 (CDN)
- **Basemap:** `topo-vector` – bản đồ địa hình vector
- **Geometry:** `Polygon`, `Polyline`, `Point` với tọa độ WGS84 (WKID 4326)
- **Symbology:** `SimpleFillSymbol`, `SimpleLineSymbol`, `PictureMarkerSymbol` (SVG data URI)
- **Popup:** `PopupTemplate` với nội dung HTML tùy chỉnh

## 📂 Cấu trúc

```
vietnam-map-2d/
└── index.html     # Ứng dụng bản đồ duy nhất (standalone)
└── README.md      # Tài liệu này
```
