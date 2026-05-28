# AIBIZ Landing Page

Landing page tinh cho AIBIZ - AI for Business Growth. Trang duoc toi uu theo huong B2B SaaS premium cho SME/CEO, tap trung vao thong diep bien AI thanh workflow, AI Agent, Automation va dashboard co the do luong.

## Cau truc du an

- `index.html` - trang landing page chinh, gom HTML/CSS/JS noi bo.
- `google-apps-script.gs` - Google Apps Script nhan lead tu form va ghi vao Google Sheet.
- `assets/` - toan bo logo, anh minh hoa va QR Zalo dang duoc trang su dung.

## Asset dang duoc su dung

Thu muc `assets/` hien chi giu cac file dang duoc `index.html` tham chieu:

- `logo-aibiz.png` - logo tren header/footer.
- `visual-ai-growth-os.png` - visual hero ben phai.
- `visual-ai-audit-score.png` - anh minh hoa muc Buoi chan doan AI cho SME.
- `visual-ai-marketing.png` - nhom AI Marketing/Content.
- `visual-ai-sales.png` - nhom AI Sales/Lead Pipeline.
- `visual-ai-automation.png` - nhom Workflow Automation.
- `visual-ai-hr.png` - nhom HR AI Assistant.
- `visual-ai-knowledge.png` - nhom Knowledge Hub.
- `visual-ai-dashboard.png` - nhom Business Dashboard.
- `visual-opc-business-os.png` - anh minh hoa OPC Business OS.
- `ngo-phu-manh.png` - anh chuyen gia.
- `zalo-qr.svg` - QR Zalo.

## Noi dung va tinh nang chinh

- Hero B2B premium voi headline 3 dong, CTA Audit AI mien phi 30 phut va visual AI Growth Operating System.
- Muc "Sau buoi Audit AI" co 4 khoi tuong tac: hover, click active, ripple va ho tro phim Enter/Space.
- Muc Audit AI 30 phut voi anh AI Audit Score va 4 dau ra ro rang.
- 6 nhom AI Business cho SME: Marketing, Sales, Automation, HR, Knowledge Hub va Dashboard.
- OPC Business OS voi anh minh hoa rieng.
- Goi giai phap, quy trinh trien khai, chuyen gia, FAQ, form dang ky va CTA cuoi trang.
- Nut Chat Zalo noi va QR Zalo trong khu vuc lien he.

## Form lead va Google Sheet

Form trong `index.html` gui du lieu qua Google Apps Script Web App bang bien:

```js
const GOOGLE_SCRIPT_URL = 'https://script.google.com/macros/s/.../exec';
```

Neu can ket noi lai voi Google Sheet khac:

1. Tao Google Sheet moi bang tai khoan muon nhan lead.
2. Trong Google Sheet, chon Extensions -> Apps Script.
3. Xoa noi dung mac dinh, dan toan bo ma trong `google-apps-script.gs`.
4. Bam Save.
5. Bam Deploy -> New deployment.
6. Chon type la Web app.
7. Execute as: Me.
8. Who has access: Anyone.
9. Bam Deploy va cap quyen truy cap cho script.
10. Copy Web app URL.
11. Mo `index.html`, tim `const GOOGLE_SCRIPT_URL`.
12. Thay URL hien tai bang Web app URL moi.

Sau khi ket noi, lead se duoc ghi vao sheet `AIBIZ Leads` va gui email thong bao ve `phumanhai@gmail.com`.

## Deploy GitHub Pages

Upload `index.html`, `google-apps-script.gs` va thu muc `assets` len repository. Bat Settings -> Pages -> Deploy from branch -> main/root.

## Ghi chu bao tri

- Khong xoa asset neu van con duoc `index.html` goi bang `src="assets/..."` hoac `url(assets/...)`.
- Khi thay anh moi, nen giu nguyen ten file asset hien co de tranh sua HTML.
- Neu thay anh hero ben phai, uu tien anh vuong 1:1 de khong bi crop.
- Neu thay anh Audit AI, uu tien anh ngang 16:9.
- Sau moi thay doi lon, nen kiem tra lai desktop va mobile, dac biet hero, muc Sau buoi Audit AI va form lead.
