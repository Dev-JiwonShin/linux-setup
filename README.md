<br> sudo find /path -name "filename" 2>/dev/null
<br> : 최상위 디렉토리부터 검색
<br> 
<br> sudo find .path -name "filename" 2>/dev/null
<br> : 현재 디렉토리부터 검색
<br> 
<br> sudo find .path -name "filename*" 2>/dev/null
<br> : 현재 디렉토리부터 검색
<br> : filename뒤에 어떤 문자열이 있든지 다 검색해줌
<br> 
<br> sudo grep -r "whatever you want. search some text in file" ~/path
<br> : 파일 내부에 특정 문자열을 검색

