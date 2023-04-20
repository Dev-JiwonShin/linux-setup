
### 최상위 디렉토리부터 검색
`sudo find /path -name "filename" 2>/dev/null`

### 현재 디렉토리부터 검색
`sudo find .path -name "filename" 2>/dev/null`

### 현재 디렉토리부터 검색
### filename뒤에 어떤 문자열이 있든지 다 검색해줌
`sudo find .path -name "filename*" 2>/dev/null`

### 파일 내부에 특정 문자열을 검색
`sudo grep -r "whatever you want. search some text in file" ~/path`

