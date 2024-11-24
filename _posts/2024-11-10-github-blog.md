---
layout: single
title: "깃헙 블로그 만들기"
---

### 글쓰기

- `_posts` 디렉터리에 파일 생성하면 된다. 
- 파일 명은 `yyyy-MM-dd-[제목].md`형식에 맞춘다. `[제목]`은 URI에 포함되기 때문에 영어로 간결하게 설정하는 것을 추천.

### 이미지 설정

#### 저장 위치 설정

1. 확장 프로그램 Paste Image 설치
    ![2024-11-24-17-53-16](/assets/images/2024-11-10-github-blog/2024-11-24-17-53-16.png){: width="45%" .align-center}

2. 아래 설정을 추가
    ```yaml
    "pasteImage.basePath": "${projectRoot}",
    "pasteImage.path": "${projectRoot}/assets/images/${currentFileNameWithoutExt}",
    "pasteImage.insertPattern": "![${imageFileNameWithoutExt}](${imageFilePath})",
    "pasteImage.forceUnixStyleSeparator": true,
    "pasteImage.prefix": "/"
    ```
3. alt + cmd + v로 이미지를 붙여넣으면 이미지 파일은 `/assets/images/` 하위의 현재 이미지를 붙여넣은 파일명 폴더 아래에 저장된다.