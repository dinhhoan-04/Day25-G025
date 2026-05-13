# card.md - Lop kien truc du lieu

**Tinh huong xu ly**: T-01, T-02, T-04, T-08

## 1. Giai phap la gi?

Thiet ke lai pipeline sang loc CV theo 5 buoc: ingest CV -> parse/normalize -> feature extraction -> fairness guardrail -> ranking + review queue. He thong them `evidence_score` va `uncertainty_score`; neu uncertainty cao thi day vao queue "Need Human Review" thay vi reject.

## 2. Vi sao sua o lop kien truc du lieu?

- Nguyen nhan goc la parse/feature chua bao phu local context va format CV da dang.
- Neu khong sua luong du lieu, prompt va UI chi giam trieu chung.

**Hanh dong phong ve chinh**:

- [x] Ngan loi bang nguon du lieu dung
- [x] Phat hien khi nguon thieu hoac loi
- [x] Khac phuc bang cach chuyen sang nguoi that
- [x] Ghi lai loi de cai thien sau

## 3. Demo nam o dau?

**File demo**: [`demo.md`](./demo.md)

Demo co:

- So do luong du lieu dau vao -> scoring -> review queue
- Binh dien rule khi parse loi/thieu du lieu
- Co che logging loi lap lai

## 4. Tac dung phu

**Co the gay van de gi?**

Tang do phuc tap he thong, do tre ranking cao hon, can quan tri them dashboard monitoring.

**Nhom giam van de do bang cach nao?**

Ap dung chi cho vi tri co rui ro cao truoc (intern/fresher volume lon), cache ket qua parse, va theo doi SLA review queue.

## 5. Checklist truoc khi nop

- [x] So do cho thay du lieu di tu dau den dau.
- [x] Co buoc kiem tra nguon truoc khi AI tra loi.
- [x] Co cach xu ly khi khong co du lieu.
- [x] Co cach chuyen sang nguoi that voi tinh huong rui ro cao.
- [x] Co cach biet loi dang lap lai.

**Nguoi phu trach**: Do Dinh Hoan
