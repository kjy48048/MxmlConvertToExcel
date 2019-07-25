# PrintFlex
- 회사에서 업무로 받은 문서화 작업을 자동화하는 자바 프로그램입니다. 
- 엄청나게 긴 플렉스 mxml 소스 코드를 보고 거기서 컴포넌트의 프로퍼티를 추출해내 문서로 기록하는 작업을 할당받았습니다. 소스가 워낙에 길고 찾으려는 부분은 작아서 굉장히 눈이 아프고 오래 걸리는 작업이었습니다. 그 업무를 수월하게 하게 위해서, 제가 찾으려는 컴포넌트의 프로퍼티만 추출해낸 뒤 보기 쉽게 출력하는 자동화 프로그램을 동료 한 명과 함께 개발했습니다. 
- 해당 소스의 파일명을 콘솔에 입력하면, 미리 입력해둔 경로를 통해서 그 파일을 찾아서 읽어옵니다. 그 파일을 찾은 뒤 내용을 String 타입으로 변환합니다. 추출을 하기 위해서 모든 String을 라인 단위로 끊어서 배열에 저장합니다. 그런 뒤 <.!-- --.> 를 찾아서 주석 부분을 삭제합니다. (주석 부분을 볼 필요가 없기 때문입니다.) 그런 뒤 컴포넌트의 소스를 읽는 작업을 시작합니다. 객체의 소스가 한 줄이라면 바로 프로퍼티를 읽어오고, 만약 한 줄 이상이라면 그 컴포넌트의 시작 부분과 끝나는 부분을 찾아서 병합시켜 한 줄로 만든 다음에 프로퍼티를 읽고 PageDTO 객체에 저장합니다. 그렇게 만들어진 PageDTO들을 배열에 저장합니다. 모든 컴포넌트의 속성을 읽고난 뒤에는 PageDTO 배열을 엑셀에 붙여놓기 쉬운 형태로 출력합니다.
이 자동화 프로그램  몇십 시간을 단축시킬 수 있었습니다.
- 2019.07.16 - 위와 관련된 업무를 또 배정받았습니다. 이번엔 여러 개의 폴더 안에 있는 모든 플렉스 파일을 읽은 뒤 중요한 프로퍼티를 찾아낸 뒤 엑셀 파일로 출력하는 업무였습니다. 이번엔 일일히 파일명을 콘솔에 입력해갈 수 없었으므로, 자동으로 파일명을 읽어오는 기능까지 개발했습니다. 또한 읽어온 데이터를 엑셀로 출력하기 위해 POI 라이브러리를 사용했습니다.
