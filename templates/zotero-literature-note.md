---
type: note
domain: other
status: draft
updated: {{importDate | format("YYYY-MM-DD")}}
citekey: "{{citekey}}"
zotero: "{{desktopURI}}"
tags:
  - zotero
  - literature
---

# {{title}}

## 서지정보

{{bibliography}}

- 저자: {% for creator in creators %}{% if creator.name %}{{creator.name}}{% else %}{{creator.firstName}} {{creator.lastName}}{% endif %}{% if not loop.last %}, {% endif %}{% endfor %}
- 발행일: {{date}}
- 인용 키: `@{{citekey}}`
- Zotero: [항목 열기]({{desktopURI}})
{% if url %}- 원문 URL: {{url}}{% endif %}
{% if DOI %}- DOI: {{DOI}}{% endif %}

{% if abstractNote %}
## 초록

{{abstractNote}}
{% endif %}

## 나의 메모

{% persist "personal-notes" %}{% if isFirstImport %}
- 이 자료의 핵심은 무엇인가?
- 오소풍_wiki의 어떤 생각과 연결되는가?
{% endif %}{% endpersist %}

## 하이라이트와 주석

{% persist "annotations" %}
{% set newAnnotations = annotations | filterby("date", "dateafter", lastImportDate) %}
{% if newAnnotations.length > 0 %}

### 가져온 시각: {{importDate | format("YYYY-MM-DD HH:mm")}}

{% for annotation in newAnnotations %}
{% if annotation.annotatedText %}
> {{annotation.annotatedText | nl2br}}
{% endif %}
{% if annotation.imageRelativePath %}
![[{{annotation.imageRelativePath}}]]
{% endif %}
{% if annotation.comment %}

**메모:** {{annotation.comment | nl2br}}
{% endif %}
{% if annotation.page %}

_페이지 {{annotation.page}}_
{% endif %}

---
{% endfor %}
{% endif %}
{% endpersist %}

## 검토 중

(초안) Zotero에서 가져온 자료를 읽고 내 언어로 정리한다.
- [ ] 감수

## 연결

- 
