# demo.md - Demo kien truc du lieu

## 1. So do cach he thong xu ly

```text
Recruiter request
  -> CV Ingestion
  -> Parser + Normalizer
      -> parse_ok ?
          -> no  -> Insufficient data + Request re-upload + log PARSE_FAIL
          -> yes -> Feature Extractor (skills/projects/impact)
                 -> Fairness Guardrail
                    - drop sensitive attributes
                    - detect risk patterns (gap year, local title mismatch)
                 -> Scoring Engine
                    -> uncertainty_score >= threshold ?
                        -> yes -> Need Human Review Queue
                        -> no  -> Shortlist recommendation
  -> UI render (confidence + reason code + evidence)
  -> Monitoring dashboard (bias flag rate, override rate, false reject rate)
```

## 2. Thanh phan chinh

| Thanh phan | Nhan gi? | Lam gi? | Tra ra gi? |
|---|---|---|---|
| Parser + Normalizer | File CV PDF/DOC | Chuan hoa text, tach section | CV_structured + parse_quality |
| Feature Extractor | CV_structured + JD | Trich skill, project, impact metric | feature_vector |
| Fairness Guardrail | feature_vector | Bo bien nhay cam, gan fairness flag | safe_features + flag |
| Scoring Engine | safe_features | Tinh match + uncertainty | score, uncertainty |
| Review Queue | score + uncertainty | Day case rui ro cho recruiter | ticket review |
| Monitoring | logs + outputs | Theo doi loi lap lai | dashboard alert |

## 3. Khi he thong gap van de

| Khi nao loi xay ra? | He thong lam gi? | Nguoi dung thay gi? |
|---|---|---|
| Nguon CV parse that bai | Dung xep hang, tao log PARSE_FAIL | "Khong du du lieu de danh gia, vui long upload lai" |
| JD khong co version moi | Dung recommendation | Banner "JD version mismatch" |
| Cau hoi vuot pham vi (yeu cau bias) | Tra refusal code POLICY_BLOCK | "Yeu cau nay khong duoc phep" |
| Fairness flag lap lai > nguong | Tao alert cho HR lead | Dashboard canh bao "Bias risk spike" |

## 4. Kiem tra nhanh

- [x] So do co buoc kiem tra cu the, khong chi "AI tra loi tot hon".
- [x] Co cach xu ly khi thieu du lieu.
- [x] Co cach chuyen sang nguoi that.
- [x] Co cach theo doi de lan sau sua tot hon.
