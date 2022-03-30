# .gitignore

.gitignore는 git이 파일을 추적할 때, 어떤 파일이나 폴더 등을 추적하지 않도록 명시하기 위해 작성하며, 해당 문서에 작성된 리스트는 수정사항이 발생해도 git이 무시하게 됩니다.

특정 파일 확장자를 무시하거나 이름에 패턴이 존재하는 경우, 또는 특정 디렉토리 아래의 모든 파일을 무시할 수 있습니다.

```
# 주석을 달기 위한 Hashtag

# MacOS Setup
.DS_Store

# Python cache files
.py[cdo]

# Important files
/Important

# AWS key
key.pem
```

생성후 .gitignore 복사붙여넣기
(https://www.toptal.com/developers/gitignore)
os (ex: macOS, window)
editor (ex: Vim, vscode)
framework (ex: react, java)
