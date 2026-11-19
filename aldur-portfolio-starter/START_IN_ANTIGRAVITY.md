# Hướng Dẫn Chuyển Dự Án Sang Google Antigravity

Thư mục này đã được đóng gói chuẩn theo cấu trúc mà **Google Antigravity** (App / IDE / CLI) tự động nhận diện (`AGENTS.md`, `GEMINI.md`, `PRD.md`, và `data/projects.json`).

## Bước 1: Mở thư mục trong Antigravity
1. Giải nén file `.zip` này ra máy tính (ví dụ đặt tên thư mục là `aldurhoang612.github.io`).
2. Mở **Google Antigravity** (hoặc **Antigravity IDE**), chọn **Open Folder** và trỏ tới thư mục vừa giải nén.
3. Antigravity sẽ **tự động đọc `AGENTS.md` / `GEMINI.md`** làm luật dự án (Workspace Rules).

## Bước 2: Copy & Dán Prompt Khởi Tạo sau vào khung Chat của Antigravity Agent

```text
Hãy đọc toàn bộ file AGENTS.md, PRD.md và data/projects.json trong workspace này.

Nhiệm vụ của bạn:
1. Lập kế hoạch triển khai (Implementation Plan) cho trang web portfolio của Aldur Hoang sử dụng Vite + React + TypeScript + Tailwind CSS (tối ưu deploy miễn phí lên GitHub Pages tại https://aldurhoang612.github.io).
2. Khởi tạo dự án và xây dựng đầy đủ giao diện Dark Mode mang phong cách điện ảnh/concert sang trọng, hỗ trợ font chữ có dấu tiếng Việt đẹp (ví dụ Space Grotesk / Plus Jakarta Sans + Be Vietnam Pro + JetBrains Mono).
3. Xây dựng đầy đủ các phần:
   - Sticky Navbar với nút chuyển đổi ngôn ngữ EN / VI.
   - Hero Section ấn tượng kèm nút mở Showreel Modal (nhúng YouTube từ data/projects.json).
   - Khu vực Selected Works đọc dữ liệu động từ data/projects.json, có bộ lọc theo 4 danh mục (Concert & Stage Visuals, Commercial Motion & LED, Brand Identity & Key Visuals, 3D Mascots/Editorial/Community) và layout Bento nổi bật cho các dự án Flagship.
   - Trang/Modal Case Study chi tiết cho từng dự án (hiển thị specs, role, studio, tools, overview, highlights, video embed nếu có, gallery và fallback card đồ họa đẹp mắt khi file ảnh trong assets/images/projects/ chưa được thả vào).
   - Khu vực About, Experience Timeline, Skills và nút tải CV.
   - Khu vực Contact kèm form liên hệ tĩnh (cấu hình sẵn Web3Forms placeholder) và các link Behance/Vimeo/Instagram/GitHub.
4. Tạo sẵn file `.github/workflows/deploy.yml` để tự động build & deploy lên GitHub Pages mỗi khi push lên nhánh `main`.
5. Chạy `npm run build` và mở trình duyệt preview của Antigravity để kiểm tra trực quan cả bản Desktop lẫn Mobile, đảm bảo không có lỗi console hay vỡ layout.
```

## Bước 3: Duyệt Kế Hoạch & Tinh Chỉnh Trực Quan
- Antigravity sẽ tạo **Implementation Plan** trước khi code — bạn có thể comment trực tiếp lên kế hoạch (ví dụ đổi màu nhấn, đổi kiểu font, hoặc đổi từ React sang HTML/CSS thuần nếu muốn).
- Sau khi Antigravity chạy bản preview trên trình duyệt tích hợp, bạn chỉ cần bảo agent tinh chỉnh trực tiếp bất kỳ chi tiết giao diện nào chưa ưng ý.

## Bước 4: Đẩy lên GitHub Pages (`aldurhoang612.github.io`)
Ngay trong Antigravity, bạn có thể gõ lệnh cho agent hỗ trợ đẩy code lên repo `https://github.com/aldurhoang612/aldurhoang612.github.io.git` (sử dụng GitHub Personal Access Token của bạn) và kiểm tra mục **Settings > Pages > Source: GitHub Actions** trên GitHub.
