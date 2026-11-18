# 요미토모 한국어 사전 데이터 (Yomitomo Korean glosses for JMdict)

크롬 확장 프로그램 「요미토모 (読み友)」가 쓰는 일본어→한국어 뜻 데이터입니다. 누구나 CC BY-SA 4.0 조건으로 쓸 수 있습니다.
Korean glosses for Japanese words, built on JMdict / OpenJLPT. Free to use under CC BY-SA 4.0 (see LICENSE, NOTICE.md).

만든 날: 2026-10-25

| 파일 | 내용 | 개수 |
|---|---|---|
| `jmdict-ko.tsv`, `jmdict-ko.json` | JMdict 항목 번호(ent_seq) → 한국어 뜻. 자주 쓰는 단어와 실제 글(뉴스·위키·소설)에 자주 나오는 단어 위주 | 42,777 |
| `jlpt-ko.tsv` | JLPT N5~N1 단어와 일상 단어: 표기·읽기·급수·한국어 뜻·예문(일본어)·예문 번역 | 9,234 |
| `kanji-ko.tsv` | 상용한자 훈음(한국어)·급수·음독·훈독 | 2,136 |

## 형식

- TSV 는 탭으로 나눈 글자 파일(첫 줄이 열 이름)입니다. 엑셀·구글 시트·Anki 에서 바로 열립니다.
- `jmdict-ko.json` 은 `{"cols": [...], "rows": [[ent_seq, kanji, reading, ko], ...]}` 꼴입니다.
- `ent_seq` 는 JMdict 의 항목 번호라서, JMdict 원본(어떤 언어판이든)과 번호로 바로 이어 붙일 수 있습니다.
- 한국어 뜻은 한 줄(2~20자), 여러 뜻은 `, ` 또는 `; ` 로 나눴습니다. 동사는 「~다」, 문법 표현은 「~」를 붙였습니다.

## 어떻게 만들었나

1. JMdict 영어판에서 빈도 표시가 있는 단어, 그리고 실제 글(위키백과 268편·아오조라 문고 20편·뉴스 515편)에서 자주 나오는 단어를 뽑았습니다.
2. 300개씩 묶어 Claude 로 한국어 뜻을 쓰고, 자동 점검(빠짐·빈값·외국 글자 섞임)과 사람 확인을 거쳤습니다.
3. 잘못된 뜻을 찾으면 알려 주세요: yomitomo.help@gmail.com

## 라이선스

CC BY-SA 4.0 — 출처를 적고, 고친 데이터도 같은 조건으로 공개하면 상업적 이용을 포함해 자유롭게 쓸 수 있습니다.
원본 데이터 출처는 `NOTICE.md` 에 있습니다.
