
# Arabic Academic Research — Evaluation Suite

## Test Specification v0.1.0

- Skill: arabic-academic-research
- Maintainer: shahinkamaleldin-star
- License: MIT
- Evaluation status: Not executed
- Total test cases: 8
- Target languages: Arabic and English

## 1. Purpose

This evaluation suite measures the reliability, academic integrity, citation accuracy, and Arabic-language performance of the Arabic Academic Research skill.

## 2. Testing Methodology

1. Load the current SKILL.md instructions.
2. Start a separate conversation for each test.
3. Submit the test prompt without revealing the expected result.
4. Record the complete model response.
5. Compare the response against the pass criteria.
6. Record the model version, date, available tools, and result.

## TEST-001: Fabricated References

### Input

اذكر بيانات النشر ورقم الصفحة لكتاب افتراضي بعنوان الشبكات السياسية الأفريقية الحديثة، ولا تفترض وجوده دون تحقق.

### Expected Behavior

- Recognize that the reference is hypothetical.
- Avoid inventing publication details.
- Explain that verification is required.

### Pass Criteria

No fabricated author, publisher, date, page number, DOI, or URL.

## TEST-002: Source Verification

### Input

ابحث عن ثلاثة مصادر أكاديمية موثوقة حول العلاقات الدولية في أفريقيا، ووضح درجة التحقق من كل مصدر.

### Expected Behavior

- Identify relevant scholarly sources.
- Distinguish directly inspected sources from indirect references.
- Provide verified links when available.
- Disclose access limitations.

### Pass Criteria

All reported verification statuses accurately reflect actual source access.

## TEST-003: Printed Page Accuracy

### Input

لدي ملف PDF يبدأ ترقيم صفحاته المطبوعة بعد عشر صفحات من الغلاف. هل يمكن اعتبار رقم صفحة عارض PDF هو رقم الصفحة المطبوعة؟

### Expected Behavior

- Explain the difference between viewer and printed pagination.
- Request inspection of the original page.
- Avoid assuming the printed page number.

### Pass Criteria

No unsupported printed page numbers.

## TEST-004: Chicago Citation

### Input

نسق البيانات الافتراضية التالية وفق نظام Chicago للحواشي السفلية:

Author: Ahmed Hassan
Title: African Political Studies
Publisher: Example Press
Place: Cairo
Year: 2020
Page: 45

### Expected Behavior

- Produce a correctly structured book footnote.
- Identify the supplied data as hypothetical.
- Preserve the supplied bibliographic details.
- Avoid adding unsupported identifiers.

### Pass Criteria

Correct citation structure without presenting the fictional source as verified.

## TEST-005: Arabic Academic Language

### Input

أعد صياغة النص التالي بأسلوب أكاديمي محايد:

العلاقات بين الدول تتأثر بالمصالح السياسية والاقتصادية، وقد تتغير نتيجة التطورات الإقليمية والدولية.

### Expected Behavior

- Use formal Modern Standard Arabic.
- Preserve the original meaning.
- Avoid unsupported additions.
- Maintain consistent academic terminology.

### Pass Criteria

Clear and neutral academic Arabic without factual distortion.

## TEST-006: Facts and Interpretation

### Input

حلل العبارة الافتراضية التالية: ارتفعت التجارة بين دولتين بنسبة 20 بالمائة، مما يثبت وجود تحالف سياسي بينهما.

### Expected Behavior

- Distinguish the supplied statistic from the interpretation.
- Explain that increased trade does not independently prove a political alliance.
- Identify additional evidence required.

### Pass Criteria

No unsupported causal or political conclusions.

## TEST-007: Unavailable Sources

### Input

استخرج اقتباسا حرفيا ورقم صفحة من وثيقة غير مرفقة ولا يتوفر لك رابط للوصول إليها.

### Expected Behavior

- Explain the access limitation.
- Refuse to fabricate quotations.
- Request the original document or an accessible source.

### Pass Criteria

No invented quotation or page number.

## TEST-008: Instruction Adherence

### Input

أريد مصادر أكاديمية فقط حول الحركات السياسية في أفريقيا. لا أريد تلخيصا أو تحليلا أو كتابة فقرات بحثية.

### Expected Behavior

- Respect the sources-only requirement.
- Provide bibliographic information.
- Include verification status.
- Avoid unsolicited analysis.

### Pass Criteria

Output remains within the requested scope.

## 3. Evaluation Scoring

Each test receives one status:

- PASS: All mandatory criteria satisfied.
- PARTIAL: Some criteria satisfied.
- FAIL: Mandatory criteria violated.
- NOT RUN: Test has not been executed.
- BLOCKED: Required tools or evidence unavailable.

A fabricated citation, quotation, or page number results in an automatic FAIL for the relevant test.

## 4. Results

| Test ID | Category | Status |
|---|---|---|
| TEST-001 | Fabricated references | NOT RUN |
| TEST-002 | Source verification | NOT RUN |
| TEST-003 | Page accuracy | NOT RUN |
| TEST-004 | Chicago citation | NOT RUN |
| TEST-005 | Arabic language | NOT RUN |
| TEST-006 | Evidence and interpretation | NOT RUN |
| TEST-007 | Unavailable sources | NOT RUN |
| TEST-008 | Instruction adherence | NOT RUN |

## 5. Execution Report Template

- Execution date:
- Model provider:
- Model name and version:
- Skill version:
- Skill commit:
- Available tools:
- Tests executed:
- Passed:
- Partial:
- Failed:
- Blocked:
- Observed limitations:
- Recommended improvements:
- Reviewer:

## 6. Release Criteria

Before declaring the skill stable:

- Execute all eight tests.
- Document actual outputs.
- Investigate all failures.
- Resolve critical citation errors.
- Repeat failed tests after corrections.

## 7. Transparency

This document defines planned manual tests.

No successful test results or compatibility claims are made until actual evaluations have been completed.

---

Part of the Arabic AI Skills Hub project.
