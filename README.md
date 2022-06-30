# git
> 깃을 잘 쓰고 싶습니다.

# Branch

# add, commit

# push, pull

# merge

# Template
## Issue
### Markdown
``` markdown
---
name: Markdown Template
about: Markdown Template
title: "[Label] Issue Title"
labels: ['bug', 'feature']
assignees: 'moonjs0113'

---

# Title
## Sub Title

- [x] Check
- [ ] Check

- list
   - sub list
```

### YAML
``` yaml
name: YAML Template
description: YAML Template Description
title: "[Label]: Issue Title"
# lable이 없을 경우에도 무시되기 때문에 존재하지 않는 label이라도 문제없다.
labels: ["bug", "triage"]
# assignees도 마찬가지로 없는 없는 경우엔 무시됨
assignees:
  - moonjs0113
# projects 는 아직 지원하지 않는건가?
body:
  - type: markdown
    attributes:
      value: |
        Thanks for taking the time to fill out this bug report!
  - type: input
    id: contact
    attributes:
      label: Contact Details
      description: How can we get in touch with you if we need more info?
      placeholder: ex. email@example.com
      # validatoins: required: true
      # 옆에 빨간별 표시된다.
      # 전부 충족되어야 issue 생성가능
    validations:
      required: false
  - type: textarea
    id: what-happened
    attributes:
      label: What happened?
      description: Also tell us, what did you expect to happen?
      placeholder: Tell us what you see!
      value: "A bug happened!"
    validations:
      required: true
  - type: dropdown
    id: version
    attributes:
      label: Version
      description: What version of our software are you running?
      options:
        - 1.0.2 (Default)
        - 1.0.3 (Edge)
    validations:
      required: true
  - type: dropdown
    id: browsers
    attributes:
      label: What browsers are you seeing the problem on?
      multiple: true
      options:
        - Firefox
        - Chrome
        - Safari
        - Microsoft Edge
  - type: textarea
    id: logs
    attributes:
      label: Relevant log output
      description: Please copy and paste any relevant log output. This will be automatically formatted into code, so no need for backticks.
      # render: shell 텍스트 속성
      render: shell
  - type: checkboxes
    id: terms
    attributes:
      label: Code of Conduct
      description: By submitting this issue, you agree to follow our [Code of Conduct](https://example.com)
      options:
        - label: I agree to follow this project's Code of Conduct
          required: true
        - label: Optional Check Box
          required: false
```

## Pull Request
![template](https://github.com/moonjs0113/git/blob/main/.github/PULL_REQUEST_TEMPLATE.md)
``` markdown
---
name: Markdown Template
about: Markdown Template
title: "[Label] Issue Title"
labels: ['bug', 'feature']
assignees: 'moonjs0113'

---

## Issues
Close Issue
Close #이슈넘버
```
