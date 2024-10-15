# 사회적 약자를 위한 인식 개선 SNS 봇

### [새싹 해커톤 - 장애인 인식개선을 위한 SNS서비스 "This Abled"](https://dacon.io/competitions/official/236293/codeshare/11391)



![dacon](assets/dacon.JPG)



### 프로젝트 개요

- 사회적 약자를 위한 생성형 AI라는 주제로 프로젝트를 진행.

  많은 사회적 약자 중 장애인이 고용에서 큰 어려움을 겪고 있는 것으로 확인되어, 인식을 개선하는 것을 통해 조금 더 많은 곳에서 고용되고 차별 받지 않는 사회를 만들고자 하였습니다.



### 데이터  설명 

- **데이터 출처** : 다양한 정부 기관에서 발행하는 `장애인식개선교육 자료 및 장애인 이해 교육자료`
  - **장애인식개선 교육자료** : 보건복지부, 한국장애인고용공단, 한국장애인개발원 등
  - **장애인 이해 교육자료** : 울산광역시교육청, 전북특별자치도교육청 등

- **설정** : PyPDF2, pptx 라이브러리를 통해 읽을 수 있는 ppt 혹은 pdf파일을 사용하였으며, 텍스트 추출 후 csv파일로 저장하여 관리

![text](assets/text.png)



### 기술 스택 

- **프로그래밍 언어** : Python

- **라이브러리** : 
  - 데이터 읽기 : PyPDF2, PyMuPDF(`fitz`), python-pdfplumber, pptx
  - 데이터 저장 : pandas, dotenv(`환경 변수`)
  - 모델 설정 : Hugging Face(`transformers, langchain`), openai(`stable diffusion`)
  - 형태소 분석기 : Kiwi (`리트리버 앙상블을 통한 검색 성능 개선`)



### 주요 결과 

- 간단한 키워드를 통한 인스타그램 게시글 생성 가능 

![ig](assets/instagram.JPG)

(실제 LLM을 통해 생성한 게시글로, 답변 관리까지 봇이 대신할 수 있도록 설계)