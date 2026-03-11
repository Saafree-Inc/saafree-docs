---
doc-type: guide
authority: informational
status: active
owner: Architecture Council
created: 2026-01-30
last-reviewed: 2026-01-30
next-review: 2026-04-30
version: 1.0
---

# Security Layer – Vai trò và Tác dụng

**Mục đích:** Mô tả vai trò chuyên biệt của Security Layer trong SaaFree OS và cách security chảy xuống domain (qua layer cha, không qua mapping trực tiếp Security Layer → 14 domain).

**Đối tượng:** Architecture Council, Chủ tịch  
**Cập nhật:** 2026-01-30

---

## 1. Vai trò của Security Layer

Security Layer được **giữ lại** với hai vai trò rõ ràng:

### 1.1 Công thức hóa và tham chiếu

- **Bản formulation chính thức:** Chứa các **layer laws** security (01–08) trong `01-layers/security/` và mapping từ Hiến pháp (`00-constitution-to-security-layer-mapping.md`).
- **Nguồn Constitution:** `08-security-supremacy.md` (S1–S8) trong `docs/01-layers/constitution/`.
- **Không map xuống 14 domain:** Yêu cầu security đến với từng domain **qua luồng dọc** Constitution 08 → Function/Logic/Physical Layer mappings → domain spec. Security Layer **không** có mapping riêng vào từng file `01-layer-to-{domain}-spec-mapping.md` cho mục đích “governance domain”; trong các file đó chỉ **ghi nhận** cách security từ Constitution 08 chảy qua layer cha xuống domain (tham chiếu Security Layer khi cần).

### 1.2 Khả năng security chuyên biệt (tương lai)

- **Lớp bảo vệ vòng ngoài:** Công cụ và kiểm soát bổ sung (runtime monitoring, anomaly detection, tích hợp kill-switch) không thuộc trách nhiệm chính của một domain Function/Logic/Physical duy nhất.
- **Marketplace và nội dung bên thứ ba:** Quét, kiểm chứng và bảo vệ **plugin đối tác** và nội dung third-party trên SaaFree marketplace; supply-chain và integrity (S8).
- Các khả năng này là **cross-cutting**, Security Layer là **chủ sở hữu** tự nhiên (tương tự “bộ chuyên trách” trong mô hình chính phủ).

---

## 2. Luồng Security (Vertical Flow)

- **Upstream:** Doctrine (Article 8, Security Section) → Constitution `08-security-supremacy.md` (S1–S8).
- **Downstream (vertical):** Constitution 08 được map trong:
  - `00-constitution-to-functional-layer-mapping.md`
  - `00-constitution-to-logical-layer-mapping.md`
  - `00-constitution-to-physical-layer-mapping.md`  
  → S1–S8 chảy vào layer laws và từ đó xuống các domain thuộc mỗi layer.
- **Security Layer:** `00-constitution-to-security-layer-mapping.md` và các luật 01–08 dùng cho **formulation chính thức** và (tương lai) **công cụ chuyên biệt**; không dùng để map trùng xuống 14 domain.

---

## 3. Cấu trúc thư mục (chỉ giữ file quan trọng)

Thư mục đã được dọn dẹp; chỉ giữ lại các file canonical:

| File | Mô tả |
|------|--------|
| `00-constitution-to-security-layer-mapping.md` | Mapping Constitution 08 → Security Layer laws 01–08 |
| `01-identity-authentication.md` … `08-human-escalation.md` | Layer laws security (S1–S8), formulation chính thức |
| `00-security-constitution.md` | Layer summary S1–S8 (English); mapping & authority flow |
| `README.md` | File này – vai trò và tác dụng của Security Layer |

Đã xóa các file thừa (guide.md, security-doctrine.md). **Doctrine chính thức:** `docs/00-doctrine/` (Article 8, Security Section). **Constitution:** `docs/01-layers/constitution/08-security-supremacy.md`.

---

## 4. Rà soát và thi công tại 14 domain

Mỗi domain có **file mapping** `01-layer-to-{domain}-spec-mapping.md` (mục Security → domain specs) và **file hướng dẫn** `00-{domain}-spec-guide.md` (mục **🔒 Security (Constitution 08) – Rà soát và thi công**). 14 team căn cứ vào hai file đó để rà soát và thi công security trong spec và runtime; chi tiết theo Appendix "Quy trình triển khai Security" trong `02-constitutional-compliance-migration-impact.md` Bước 4.

---

**Duy trì bởi:** Architecture Council  
**Cập nhật:** 2026-01-30
