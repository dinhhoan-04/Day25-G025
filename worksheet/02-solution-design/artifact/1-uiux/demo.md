# demo.md - Demo giao dien

## 1. Man hinh chinh

```text
+--------------------------------------------------------------------------------+
| CV Screen Assist - Shortlist Round 1                                           |
+--------------------------------------------------------------------------------+
| Candidate            | Match Score | Confidence | Fairness Flag | Action       |
|---------------------|-------------|------------|---------------|--------------|
| Nguyen A             | 82          | High       | None          | Shortlist     |
| Tran B (gap year)    | 78          | Low        | Review needed | RequestReview |
| Le C (local school)  | 76          | Low        | Review needed | RequestReview |
+--------------------------------------------------------------------------------+
| Note: "Shortlist so bo. Recruiter phai review 20% CV ngoai top de tranh bo sot"|
| [View Evidence] [Escalate to Recruiter Lead] [Export shortlist]                |
+--------------------------------------------------------------------------------+
```

## 2. Trang thai can minh hoa

| Trang thai | Nguoi dung thay gi? | Nguoi dung lam gi tiep? |
|---|---|---|
| Co nguon xac minh | Badge xanh "Evidence linked" + score reason | Co the shortlist binh thuong |
| Chua co nguon xac minh | Badge vang "Need review" + nut Reject bi khoa | Bam RequestReview |
| AI khong nen tu tra loi | Banner do "Insufficient evidence" | Escalate cho recruiter lead |
| Can chuyen sang nguoi that | CTA "Escalate" hien SLA 24h | Gui case cho nguoi duyet |

## 3. Ghi chu cho tung thanh phan

- `Confidence`: hien theo High/Medium/Low dua tren do day du evidence.
- `Fairness Flag`: bat neu phat hien pattern de bi bias (gap year, format la, local context).
- `RequestReview`: thay cho `Reject` khi flag dang bat.

## 4. Kiem tra nhanh

- [x] Nhin vao demo la hieu rui ro dang duoc chan o dau.
- [x] Co trang thai khi AI khong co du thong tin.
- [x] Co cach chuyen sang nguoi that.
- [x] Cau chu ngan de dat tren man hinh that.
