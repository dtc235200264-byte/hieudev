<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CV - Đặng Hữu Hiếu - Software Engineer Fresher</title>
  <style>
    :root {
      --primary: #1e3a8a;
      --primary-light: #eff6ff;
      --primary-border: #bfdbfe;
      --text-main: #1f2937;
      --text-muted: #4b5563;
      --text-light: #6b7280;
      --accent: #2563eb;
    }

    [data-theme="emerald"] {
      --primary: #065f46;
      --primary-light: #ecfdf5;
      --primary-border: #a7f3d0;
      --accent: #059669;
    }

    [data-theme="indigo"] {
      --primary: #3730a3;
      --primary-light: #eef2ff;
      --primary-border: #c7d2fe;
      --accent: #4f46e5;
    }

    [data-theme="slate"] {
      --primary: #0f172a;
      --primary-light: #f8fafc;
      --primary-border: #cbd5e1;
      --accent: #334155;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
      background-color: #e5e7eb;
      color: var(--text-main);
      line-height: 1.5;
      font-size: 13.5px;
      -webkit-font-smoothing: antialiased;
    }

    .toolbar {
      position: sticky;
      top: 0;
      z-index: 100;
      background: #ffffff;
      border-bottom: 1px solid #d1d5db;
      padding: 10px 20px;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
      gap: 12px;
      box-shadow: 0 2px 4px rgba(0,0,0,0.08);
    }

    .toolbar-left, .toolbar-right {
      display: flex;
      align-items: center;
      gap: 10px;
      flex-wrap: wrap;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      padding: 7px 14px;
      border-radius: 6px;
      font-size: 13px;
      font-weight: 500;
      cursor: pointer;
      border: 1px solid transparent;
      transition: all 0.2s;
    }

    .btn-primary {
      background: var(--accent);
      color: #ffffff;
    }

    .btn-primary:hover {
      opacity: 0.9;
    }

    .btn-secondary {
      background: #ffffff;
      border-color: #d1d5db;
      color: #374151;
    }

    .theme-picker {
      display: flex;
      align-items: center;
      gap: 6px;
      font-size: 12px;
      color: #4b5563;
    }

    .theme-dot {
      width: 18px;
      height: 18px;
      border-radius: 50%;
      cursor: pointer;
      border: 2px solid #ffffff;
      box-shadow: 0 0 0 1px #d1d5db;
    }

    .theme-dot:hover {
      transform: scale(1.15);
    }

    .edit-hint {
      font-size: 11.5px;
      color: #065f46;
      background: #d1fae5;
      padding: 3px 8px;
      border-radius: 4px;
      border: 1px solid #a7f3d0;
    }

    .page-wrapper {
      padding: 24px 12px 60px;
      display: flex;
      justify-content: center;
    }

    .cv-container {
      width: 210mm;
      min-height: 297mm;
      background: #ffffff;
      box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.15);
      padding: 22mm 18mm;
      display: flex;
      flex-direction: column;
      gap: 15px;
    }

    [contenteditable="true"]:hover {
      outline: 1.5px dashed var(--accent);
      outline-offset: 2px;
      border-radius: 2px;
      background-color: rgba(37, 99, 235, 0.03);
    }

    [contenteditable="true"]:focus {
      outline: 2px solid var(--accent);
      outline-offset: 2px;
      border-radius: 2px;
      background-color: rgba(37, 99, 235, 0.05);
    }

    .cv-header {
      border-bottom: 2px solid var(--primary);
      padding-bottom: 12px;
    }

    .name-role h1 {
      font-size: 25px;
      font-weight: 700;
      color: var(--primary);
      text-transform: uppercase;
      letter-spacing: 0.5px;
      margin-bottom: 3px;
    }

    .name-role h2 {
      font-size: 14.5px;
      font-weight: 600;
      color: var(--accent);
      margin-bottom: 8px;
    }

    .contact-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 5px 16px;
      font-size: 12.5px;
      color: var(--text-muted);
    }

    .contact-item {
      display: inline-flex;
      align-items: center;
      gap: 6px;
    }

    .icon {
      width: 14px;
      height: 14px;
      flex-shrink: 0;
      stroke: var(--accent);
    }

    .section-title {
      font-size: 13.5px;
      font-weight: 700;
      color: var(--primary);
      text-transform: uppercase;
      letter-spacing: 0.8px;
      border-bottom: 1.5px solid var(--primary-border);
      padding-bottom: 3px;
      margin-bottom: 7px;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .section-title svg {
      width: 15px;
      height: 15px;
      stroke: var(--accent);
    }

    .objective-text {
      text-align: justify;
      color: var(--text-muted);
      line-height: 1.6;
    }

    .skills-list {
      display: flex;
      flex-direction: column;
      gap: 5px;
    }

    .skill-row {
      display: grid;
      grid-template-columns: 140px 1fr;
      align-items: baseline;
      gap: 8px;
      font-size: 13px;
    }

    .skill-label {
      font-weight: 600;
      color: var(--text-main);
    }

    .skill-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 5px;
    }

    .badge {
      font-size: 11.5px;
      background: var(--primary-light);
      color: var(--primary);
      padding: 2px 7px;
      border-radius: 4px;
      font-weight: 500;
      border: 1px solid var(--primary-border);
    }

    .item-block {
      margin-bottom: 10px;
    }

    .item-block:last-child {
      margin-bottom: 0;
    }

    .item-header {
      display: flex;
      justify-content: space-between;
      align-items: baseline;
      margin-bottom: 2px;
    }

    .item-title {
      font-size: 13.5px;
      font-weight: 700;
      color: var(--text-main);
    }

    .item-subtitle {
      font-size: 12.5px;
      font-weight: 600;
      color: var(--accent);
    }

    .item-date {
      font-size: 12px;
      color: var(--text-light);
      font-style: italic;
    }

    .item-meta {
      font-size: 12px;
      color: var(--text-muted);
      margin-bottom: 4px;
      display: flex;
      gap: 12px;
    }

    .item-bullet-list {
      list-style-type: disc;
      padding-left: 17px;
      color: var(--text-muted);
      font-size: 12.8px;
    }

    .item-bullet-list li {
      margin-bottom: 3px;
      line-height: 1.5;
    }

    .item-bullet-list strong {
      color: var(--text-main);
    }

    .project-tech {
      font-size: 12px;
      color: var(--text-light);
      margin-bottom: 3px;
    }

    .project-links {
      display: inline-flex;
      gap: 10px;
      font-size: 11.5px;
      margin-left: 8px;
    }

    .project-links a {
      color: var(--accent);
      text-decoration: none;
    }

    @media print {
      body {
        background: #ffffff !important;
      }
      .toolbar, .no-print {
        display: none !important;
      }
      .page-wrapper {
        padding: 0 !important;
        margin: 0 !important;
      }
      .cv-container {
        width: 100% !important;
        box-shadow: none !important;
        padding: 6mm 10mm !important;
      }
      @page {
        size: A4 portrait;
        margin: 6mm 8mm;
      }
      .item-block, .cv-section {
        page-break-inside: avoid;
      }
    }
  </style>
</head>
<body>

  <header class="toolbar no-print">
    <div class="toolbar-left">
      <button class="btn btn-primary" onclick="window.print()">
        <svg class="icon" style="stroke: #fff;" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <polyline points="6 9 6 2 18 2 18 9"></polyline>
          <path d="M6 18H4a2 2 0 0 1-2-2v-5a2 2 0 0 1 2-2h16a2 2 0 0 1 2 2v5a2 2 0 0 1-2 2h-2"></path>
          <rect x="6" y="14" width="12" height="8"></rect>
        </svg>
        In / Xuất PDF (A4)
      </button>
      <span class="edit-hint">✅ Đã cập nhật tên Đặng Hữu Hiếu. Bạn có thể bấm In / Xuất PDF ngay!</span>
    </div>

    <div class="toolbar-right">
      <div class="theme-picker">
        <span>Màu sắc:</span>
        <div class="theme-dot" style="background:#1e3a8a;" onclick="setTheme('')" title="Navy"></div>
        <div class="theme-dot" style="background:#065f46;" onclick="setTheme('emerald')" title="Emerald"></div>
        <div class="theme-dot" style="background:#3730a3;" onclick="setTheme('indigo')" title="Indigo"></div>
        <div class="theme-dot" style="background:#0f172a;" onclick="setTheme('slate')" title="Slate"></div>
      </div>
      <button class="btn btn-secondary" onclick="saveToLocal()">Lưu</button>
      <button class="btn btn-secondary" onclick="resetDefault()">Đặt lại</button>
    </div>
  </header>

  <main class="page-wrapper">
    <div id="cvContent" class="cv-container">
      
      <section class="cv-header">
        <div class="name-role">
          <h1 contenteditable="true">ĐẶNG HỮU HIẾU</h1>
          <h2 contenteditable="true">SOFTWARE ENGINEER / FULLSTACK DEVELOPER FRESHER</h2>
        </div>

        <div class="contact-grid">
          <div class="contact-item">
            <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path>
              <polyline points="22,6 12,13 2,6"></polyline>
            </svg>
            <span contenteditable="true">danghuuhieu.dev@gmail.com</span>
          </div>

          <div class="contact-item">
            <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"></path>
            </svg>
            <span contenteditable="true">(+84) 0968 123 456</span>
          </div>

          <div class="contact-item">
            <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path>
            </svg>
            <span contenteditable="true">github.com/hieu-dev</span>
          </div>

          <div class="contact-item">
            <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"></path>
              <rect x="2" y="9" width="4" height="12"></rect>
              <circle cx="4" cy="4" r="2"></circle>
            </svg>
            <span contenteditable="true">linkedin.com/in/hieudev-se</span>
          </div>

          <div class="contact-item">
            <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <circle cx="12" cy="12" r="10"></circle>
              <line x1="2" y1="12" x2="22" y2="12"></line>
              <path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"></path>
            </svg>
            <span contenteditable="true">hieudev-portfolio.vercel.app</span>
          </div>

          <div class="contact-item">
            <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"></path>
              <circle cx="12" cy="10" r="3"></circle>
            </svg>
            <span contenteditable="true">Hà Nội, Việt Nam</span>
          </div>
        </div>
      </section>

      <section class="cv-section">
        <h3 class="section-title">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"></circle><polyline points="12 6 12 12 16 14"></polyline></svg>
          Mục Tiêu Nghề Nghiệp
        </h3>
        <p class="objective-text" contenteditable="true">
          Tốt nghiệp chuyên ngành Kỹ thuật Phần mềm với nền tảng vững vàng về Cấu trúc dữ liệu & Giải thuật, lập trình hướng đối tượng (OOP) và phát triển ứng dụng Web fullstack (ReactJS, Node.js, RESTful API). Có kinh nghiệm thực tế qua các đồ án phần mềm đạt điểm xuất sắc và kỳ thực tập doanh nghiệp. Mong muốn gia nhập đội ngũ phát triển với vị trí Software Engineer Fresher để cống hiến vào các sản phẩm thực tế, rèn luyện tư duy Clean Architecture và nâng cao kỹ năng Cloud/DevOps.
        </p>
      </section>

      <section class="cv-section">
        <h3 class="section-title">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="16 18 22 12 16 6"></polyline><polyline points="8 6 2 12 8 18"></polyline></svg>
          Kỹ Năng Chuyên Môn
        </h3>
        <div class="skills-list" contenteditable="true">
          <div class="skill-row">
            <span class="skill-label">Ngôn ngữ lập trình:</span>
            <div class="skill-tags">
              <span class="badge">JavaScript / TypeScript</span>
              <span class="badge">Java</span>
              <span class="badge">HTML5 / CSS3 / SCSS</span>
              <span class="badge">SQL</span>
            </div>
          </div>
          <div class="skill-row">
            <span class="skill-label">Frontend & UI:</span>
            <div class="skill-tags">
              <span class="badge">React.js</span>
              <span class="badge">Next.js</span>
              <span class="badge">TailwindCSS</span>
              <span class="badge">Redux Toolkit</span>
              <span class="badge">Responsive Design</span>
            </div>
          </div>
          <div class="skill-row">
            <span class="skill-label">Backend & Database:</span>
            <div class="skill-tags">
              <span class="badge">Node.js / Express</span>
              <span class="badge">RESTful API Design</span>
              <span class="badge">PostgreSQL</span>
              <span class="badge">MongoDB</span>
              <span class="badge">Prisma ORM</span>
            </div>
          </div>
          <div class="skill-row">
            <span class="skill-label">Công cụ & Quy trình:</span>
            <div class="skill-tags">
              <span class="badge">Git / GitHub</span>
              <span class="badge">Postman</span>
              <span class="badge">Docker (Cơ bản)</span>
              <span class="badge">Linux CLI</span>
              <span class="badge">Agile / Scrum</span>
            </div>
          </div>
        </div>
      </section>

      <section class="cv-section">
        <h3 class="section-title">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polygon points="12 2 2 7 12 12 22 7 12 2"></polygon><polyline points="2 17 12 22 22 17"></polyline><polyline points="2 12 12 17 22 12"></polyline></svg>
          Dự Án Nổi Bật
        </h3>
        <div contenteditable="true">
          
          <div class="item-block">
            <div class="item-header">
              <div>
                <span class="item-title">E-Commerce Web Platform (Nền tảng Mua sắm Trực tuyến)</span>
                <span class="project-links">[<a href="https://github.com" target="_blank">Demo</a>] [<a href="https://github.com" target="_blank">GitHub</a>]</span>
              </div>
              <span class="item-date">09/2024 - 12/2024</span>
            </div>
            <div class="project-tech"><strong>Công nghệ:</strong> React.js, TailwindCSS, Node.js, Express, MongoDB, Redux Toolkit, JWT</div>
            <ul class="item-bullet-list">
              <li>Xây dựng ứng dụng web thương mại điện tử fullstack với tính năng duyệt danh mục sản phẩm, bộ lọc đa điều kiện, giỏ hàng và thanh toán trực tuyến mô phỏng.</li>
              <li>Thiết kế hệ thống xác thực an toàn bằng <strong>JWT & HTTP-only Cookies</strong>, mã hóa mật khẩu với Bcrypt và phân quyền người dùng (User & Admin).</li>
              <li>Phát triển trang Dashboard quản trị cho phép theo dõi doanh thu biểu đồ trực quan, quản lý kho sản phẩm và cập nhật trạng thái đơn hàng tức thì.</li>
              <li>Tối ưu hóa hình ảnh webp và lazy-loading các component giúp cải thiện điểm <strong>Google Lighthouse Performance đạt 94/100</strong>.</li>
            </ul>
          </div>

          <div class="item-block">
            <div class="item-header">
              <div>
                <span class="item-title">Collaborative Task Board (Bảng Quản Lý Công Việc Nhóm Thời Gian Thực)</span>
                <span class="project-links">[<a href="https://github.com" target="_blank">Demo</a>] [<a href="https://github.com" target="_blank">GitHub</a>]</span>
              </div>
              <span class="item-date">03/2024 - 06/2024</span>
            </div>
            <div class="project-tech"><strong>Công nghệ:</strong> TypeScript, Next.js, PostgreSQL, Prisma ORM, Socket.io, TailwindCSS</div>
            <ul class="item-bullet-list">
              <li>Thiết kế ứng dụng tương tự Trello, hỗ trợ kéo thả thẻ công việc (Drag & Drop) mượt mà giữa các cột trạng thái dự án.</li>
              <li>Tích hợp <strong>Socket.io</strong> để đồng bộ hóa trạng thái thẻ và bình luận tức thì giữa nhiều người dùng trong nhóm mà không cần tải lại trang.</li>
              <li>Chuẩn hóa cấu trúc cơ sở dữ liệu quan hệ với PostgreSQL và Prisma ORM, tối ưu hóa index các trường thường xuyên query giúp giảm 40% độ trễ API.</li>
            </ul>
          </div>

        </div>
      </section>

      <section class="cv-section">
        <h3 class="section-title">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="7" width="20" height="14" rx="2" ry="2"></rect><path d="M16 21V5a2 2 0 0 0-2-2h-4a2 2 0 0 0-2 2v16"></path></svg>
          Kinh Nghiệm Thực Tế & Hoạt Động
        </h3>
        <div contenteditable="true">
          <div class="item-block">
            <div class="item-header">
              <span class="item-title">Thực tập sinh Lập trình Web (Web Developer Intern)</span>
              <span class="item-date">06/2024 - 09/2024</span>
            </div>
            <div class="item-subtitle">Công ty Cổ phần Công nghệ FPT Software - Hà Nội</div>
            <ul class="item-bullet-list">
              <li>Tham gia phát triển module quản lý người dùng và bảng điều khiển nội bộ sử dụng React.js và Ant Design dưới sự hướng dẫn của Senior Engineer.</li>
              <li>Tích hợp và kiểm thử hơn 15 RESTful endpoints, bắt lỗi dữ liệu đầu vào và hiển thị thông báo thân thiện cho người dùng.</li>
              <li>Thực hành quy trình Git flow chuyên nghiệp (pull request, review code chéo và giải quyết merge conflicts).</li>
            </ul>
          </div>

          <div class="item-block">
            <div class="item-header">
              <span class="item-title">Thành viên Ban Chuyên môn - CLB Tin học & Sáng tạo Phần mềm</span>
              <span class="item-date">2022 - 2024</span>
            </div>
            <div class="item-subtitle">Trường Đại học Bách Khoa Hà Nội</div>
            <ul class="item-bullet-list">
              <li>Hỗ trợ hướng dẫn thực hành cho hơn 40 sinh viên khóa dưới trong chuỗi workshop "Nhập môn Git/GitHub & Lập trình Web cơ bản".</li>
              <li>Đạt <strong>Top 10</strong> cuộc thi Hackathon Sinh viên sáng tạo công nghệ 2023 với đề tài ứng dụng hỗ trợ học tập trực tuyến.</li>
            </ul>
          </div>
        </div>
      </section>

      <section class="cv-section">
        <h3 class="section-title">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M22 10v6M2 10l10-5 10 5-10 5z"></path><path d="M6 12v5c3 3 9 3 12 0v-5"></path></svg>
          Học Vấn & Chứng Chỉ
        </h3>
        <div contenteditable="true">
          <div class="item-block">
            <div class="item-header">
              <span class="item-title">Đại Học Bách Khoa Hà Nội</span>
              <span class="item-date">2021 - 2025</span>
            </div>
            <div class="item-subtitle">Cử nhân Kỹ thuật Phần mềm (Chương trình Tiên tiến)</div>
            <div class="item-meta">
              <span>Điểm GPA: <strong>3.42 / 4.0</strong> (Xếp loại Giỏi)</span>
              <span>•</span>
              <span>Đạt học bổng Khuyến khích học tập 2 học kỳ liên tiếp</span>
            </div>
          </div>

          <div class="item-block">
            <div class="item-header">
              <span class="item-title">Chứng chỉ chuyên môn & Ngoại ngữ</span>
              <span class="item-date">2023 - 2024</span>
            </div>
            <ul class="item-bullet-list">
              <li><strong>TOEIC 780 / 990:</strong> Đọc hiểu tài liệu kỹ thuật tiếng Anh tốt, tự tin giao tiếp trong công việc.</li>
              <li><strong>HackerRank Problem Solving (Intermediate):</strong> Nắm vững thuật toán và cấu trúc dữ liệu.</li>
              <li><strong>Meta Front-End Developer Professional Certificate</strong> (Coursera).</li>
            </ul>
          </div>
        </div>
      </section>

    </div>
  </main>

  <script>
    function setTheme(theme) {
      if (theme) {
        document.documentElement.setAttribute('data-theme', theme);
      } else {
        document.documentElement.removeAttribute('data-theme');
      }
    }

    const KEY = 'cv_user_data_local';
    function saveToLocal() {
      localStorage.setItem(KEY, document.getElementById('cvContent').innerHTML);
      alert('Đã lưu nội dung CV thành công!');
    }

    function resetDefault() {
      if (confirm('Khôi phục lại nội dung ban đầu?')) {
        localStorage.removeItem(KEY);
        location.reload();
      }
    }

    window.addEventListener('DOMContentLoaded', () => {
      const saved = localStorage.getItem(KEY);
      if (saved) document.getElementById('cvContent').innerHTML = saved;
    });

    document.addEventListener('focusout', (e) => {
      if (e.target.isContentEditable) {
        localStorage.setItem(KEY, document.getElementById('cvContent').innerHTML);
      }
    });
  </script>
</body>
</html>
