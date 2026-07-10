# 🇻🇳 Skill Thuế TNCN Vietnam (2026)

> AI Skill tra cứu thuế TNCN, SOP kê khai/quyết toán, hướng dẫn theo nhóm đối tượng.

[![Version](https://img.shields.io/badge/version-1.11.0-blue)]()
[![License](https://img.shields.io/badge/license-MIT-green)]()
[![Score](https://img.shields.io/badge/audit%20score-9.5%2F10-brightgreen)]()
[![Updated](https://img.shields.io/badge/updated-11%2F07%2F2026-orange)]()

## Tổng Quan

Skill **thue-tncn-vietnam** là bộ công cụ tra cứu thuế TNCN dạng AI, tự chứa toàn bộ dữ liệu cần thiết. Hoạt động trên Claude Desktop, Google Antigravity, và các nền tảng AI hỗ trợ skill/knowledge base.

### Tính năng chính

- 📊 **Biểu thuế 5 bậc 2026** (Luật 109/2025/QH15)
- 🧮 **9 case study tính thuế** chi tiết (lương, freelancer, KOL, tài sản số, expat, làm thêm giờ, giảm trừ y tế/giáo dục)
- 📋 **SOP quyết toán** qua eTax Mobile (9 bước) + Cổng thuế (5 bước)
- 🌏 **Thuế người nước ngoài** (cư trú/không cư trú, DTA, flat 20%, lợi ích tiền ăn/thuê nhà)
- 🏠 **Thuế bất động sản** (miễn thuế nhà đất duy nhất sở hữu tối thiểu 183 ngày, miễn thuế khi ly hôn chia tài sản)
- 📈 **Thuế chứng khoán phái sinh** (thuế suất 0,1% trên hợp đồng tương lai từng lần)
- 🔒 **3 Verification Gates + 8 Anti-Hallucination Rules** chống sai sót
- ✅ **Calculation Checklist** 9 bước bắt buộc trước khi output phép tính
- 💰 **BHXH rút 1 lần** (công thức tính, điều kiện 2 nhóm, 4 case study)
- 🛡️ **Trợ cấp thất nghiệp (BHTN)** (công thức 60% lương, thời gian hưởng, quy trình đăng ký)

### Nhóm đối tượng

| Nhóm | File hướng dẫn |
|------|---------------|
| Người làm công ăn lương | `tong-quan-thue.md` + `sop-quyet-toan.md` |
| Freelancer / KOL / Seller | `freelancer-guide.md` |
| Người nước ngoài (Expat) | `nguoi-nuoc-ngoai-guide.md` |
| Nghỉ việc / rút BHXH | `bhxh-rut-mot-lan-guide.md` |
| Thất nghiệp / BHTN | `bhtn-tro-cap-guide.md` |
| Người giao dịch bất động sản | `bat-dong-san-guide.md` |
| Người đầu tư phái sinh | `chung-khoan-phai-sinh-guide.md` |

## Cài Đặt

### Claude Desktop / Antigravity

```
your-project/
└── .agents/
    └── skill/
        └── thue-tncn-vietnam/   ← copy vào đây
```

### Các nền tảng khác

Copy nội dung `SKILL.md` vào system prompt, upload folder `references/` vào knowledge base.

## Số Liệu Nhanh (2026)

| Chỉ số | Giá trị | Căn cứ |
|--------|---------|--------|
| Giảm trừ bản thân | 15,5 tr/tháng | NQ 110/2025/UBTVQH15 |
| Giảm trừ NPT | 6,2 tr/tháng | NQ 110/2025/UBTVQH15 |
| Thu nhập tối đa NPT | Không quá **3 tr/tháng** (cũ: 1tr) | TT 87/2026/TT-BTC |
| Khấu trừ vãng lai 10% | Từ **5 tr/lần trở lên** (cũ: 2tr) | TT 87/2026/TT-BTC |
| Khống chế tiền ăn ca | Tối đa **1,2 tr/tháng** (cũ: 730k) | NĐ 253/2026/NĐ-CP |
| Giảm trừ hưu trí tự nguyện | Tối đa **3 tr/tháng** (cũ: 1tr) | NĐ 253/2026/NĐ-CP |
| Giảm trừ Y tế | Tối đa **23 tr/năm** (mới) | NĐ 253/2026/NĐ-CP |
| Giảm trừ Giáo dục | Tối đa **24 tr/năm** (mới) | NĐ 253/2026/NĐ-CP |
| Thuế phái sinh (HĐTL) | **0,1%** giá chuyển nhượng | TT 87/2026/TT-BTC |
| Ngưỡng miễn thuế HKD | **1 tỷ/năm** (cũ: 500tr) | NĐ 141/2026/NĐ-CP |
| Trần đóng BHXH/BHYT | **50,6 triệu/tháng** (lương cơ sở 2,53tr từ 01/07/2026) | NĐ 161/2026/NĐ-CP |
| Biểu thuế lũy tiến | 5 bậc (5% - 35%) | Luật 109/2025/QH15 |
| Thuế khoán | **Bãi bỏ** từ 01/01/2026 | NQ 198/2025/QH15 |

## Cấu Trúc

```
thue-tncn-vietnam/
├── SKILL.md                          ← Master file (AI đọc đầu tiên)
├── README.md                         ← File này
├── pending-review/                   ← Văn bản mới chờ duyệt
└── references/
    ├── tong-quan-thue.md             ← Biểu thuế, giảm trừ, ngưỡng, chi phí YT/GD
    ├── vi-du-tinh-thue.md            ← 9 ví dụ tính thuế chi tiết
    ├── sop-quyet-toan.md             ← SOP quyết toán eTax / Cổng thuế
    ├── freelancer-guide.md           ← Freelancer, KOL, seller, tài sản số
    ├── nguoi-nuoc-ngoai-guide.md     ← Expat, cư trú, DTA
    ├── thue-khoan-guide.md           ← Thuế khoán bãi bỏ 2026
    ├── bat-dong-san-guide.md         ← Thuế BĐS, nhà đất duy nhất, ly hôn (Mới)
    ├── chung-khoan-phai-sinh-guide.md← Thuế chứng khoán phái sinh 0,1% (Mới)
    ├── deadline-tracker.md           ← Lịch nộp thuế 2026
    ├── faq.md                        ← 15 câu hỏi thường gặp (bổ sung tài khoản ngân hàng)
    ├── bhxh-rut-mot-lan-guide.md     ← BHXH rút 1 lần: điều kiện, công thức, case study
    ├── bhtn-tro-cap-guide.md         ← Trợ cấp thất nghiệp: công thức, quy trình
    ├── system-flow.md                ← Flow diagrams (Mermaid)
    ├── changelog.md                  ← Lịch sử cập nhật + expiry
    └── sources.md                    ← Nguồn tham khảo
```

## Audit Score

Skill đã qua **5 vòng đánh giá** theo quy trình 6 bước:

```
v1.4.0 (7.4) → v1.5.0 (7.9) → v1.6.0 (8.7) → v1.7.0 (9.2) → v1.8.0 → v1.9.0 (+BHXH/BHTN) → v1.9.1 (+Luật 09/2026/QH16) → v1.10.0 (Lương cơ sở 2.53tr) → v1.11.0 (Quy định chi tiết NĐ 253/2026 & TT 87/2026)
```

## Lưu Ý Quan Trọng

⚠️ **Thông tin chỉ mang tính tham khảo, KHÔNG thay thế tư vấn thuế chuyên nghiệp.**

Kiểm tra lại tại:
- https://gdt.gov.vn
- https://canhan.gdt.gov.vn

## Tác Giả

**Minh Đỗ** | [Liên hệ](https://facebook.com/dotanminh)

---

*Cập nhật: 11/07/2026 | Lương cơ sở 2,53tr | Luật 109/2025/QH15 | Luật 09/2026/QH16 | NĐ 253/2026/NĐ-CP | TT 87/2026/TT-BTC | NĐ 141/2026/NĐ-CP | NĐ 68/2026/NĐ-CP*
