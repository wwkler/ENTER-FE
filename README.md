# KT 에이블스쿨 4기 빅프로젝트

## 1. 주제
**고객 만족도조사 자동화: 내 손안의 전략 수립 파트너-ENTER**
- 자사 제품 및 서비스의 객관적인 진단을 확인하기 위해서 겪는 과정은 험난하다. 시간과 비용이 많이 들어가며, 과연 진단이 제대로 됐는가에 대한 의문 제기 가능
- 설문조사에 따른 데이터보다 인터넷, 커뮤니티에 따른 데이터를 활용하여 데이터베이스를 구축하고 LLM를 활용하여 새로운 인사이트를 도출하여 전략 수립에 활용
- 미래에 대한 전략 수립을 저비용으로 신속하게 진행하고자 하는 기업, 자사의 제품 서비스와 경쟁사 제품 서비스를 비교 분석하는 기업 사용 가능
- 수집된 실사용 데이터의 분석 결과를 통해 개선 사항, 타겟 세분화, 광고 제작 가이드, 예상 판매량 등 수많은 솔루션 도출 가능
  
<p float="left">
  ![17조  4기 17조 소개이미지 (1)](https://github.com/user-attachments/assets/354dde58-7197-4814-9320-ed760432e065)
  
  ![17조  4기 17조 썸네일](https://github.com/user-attachments/assets/2a2d28e7-2b77-4607-b724-6db75ad3497b)
</p>


## 2. 서비스 내용
- 여러 곳의 웹사이트에서 실사용자의 사용기, 리뷰를 스크래핑
   - 키워드 기반으로 검색하여 해당 키워드에 맞는 게시글을 모두 스크랩
- 자사에 필요한 데이터를 분류하기 위한 llama2 사용
   - 로컬에 구성하여 사용할 수 있는 llm모델
   - 수집해도 의미가 없는 데이터와 수집 해야할 데이터를 선별하기 위해 사용
   - ChatGPT로 해당 태스크 진행 시 수백, 수천 건의 데이터를 API호출 시 비용문제와, 네트워크 에러 시 작동이 멈출 수 있음
   - 대조적으로 llama2는 로컬에 구성하여 GPU를 통한 구동은 물론CPU가동도 가능하기 때문에, 비교적 저비용으로 투자한 리소스에서도 실행이 가능하며, 한 번 구축하면 장기적으로 활용이 가능
- 수집된 데이터를 기반으로 Vector DB 파이프 라인 구축
   - 사용자가 요청한 질문에 대해서 ChatGPT가 수집된 리뷰 데이터에서 유사한 데이터를 참조하여 답변을 생성하기 위한 vector DB 파이프라인 구축
- 수집된 데이터에 대해 프롬프트와 동일한 환경에서 질문 수행
- 적재된 VectorDB에서 실사용 데이터를 참조해 질문에 대한 답변 생성 및 도출
- 수집된 실사용 데이터를 기반으로 여러가지 분석 기법을 적용한 리포트 생성 및 다운로드

![service-flow](https://github.com/user-attachments/assets/e4803b79-4415-4a34-b61b-59b00b3bccdd)




## 3. 기술 스택

![tool-stack](https://github.com/user-attachments/assets/3b6d1880-9993-4394-a0a9-77a59341f399)


## 4. 기능
   - 프롬프트
     
   ![main_prompt](https://github.com/user-attachments/assets/e42cc0db-91b2-493c-9ae8-cdcecff0917f)

   &nbsp;
   
   - 크롤러 설정(수집 대상 선택)
     
   ![crawler_config](https://github.com/user-attachments/assets/6a12710a-d888-403f-92c6-45cd632aa94d)

    
   &nbsp;

   - 크롤러 설정(수집 대상 크롤링 데이터 확인)

   ![crawler_info_show](https://github.com/user-attachments/assets/b0c96c3c-95a4-4cce-be98-dc1365d56fbe)

    
   &nbsp;

   - 크롤러 설정(크롤러 템플릿 설정)
     
   ![crawler_template](https://github.com/user-attachments/assets/c0fc263f-f283-4564-a3ba-f4b4d7b17135)


   &nbsp;

   - 프롬프트 설정
     
   ![prompt_config](https://github.com/user-attachments/assets/ce623d35-64e4-4dda-b37c-698c9ee137bb)


   &nbsp;

   - 레포트 설정
     
   ![report_config](https://github.com/user-attachments/assets/c1475aa8-12ce-4116-97e2-dc4335c79cca)

   &nbsp;

   - 모델 설정
     
   ![model_config](https://github.com/user-attachments/assets/b53f8de7-d880-4067-9dae-59215802369b)


   &nbsp;
     
## 5. 개발 일정

![develop_time](https://github.com/user-attachments/assets/925502d7-ff59-4d02-aaaa-99658a4abfb6)





## 6. 느낀점
- GitHub를 활용하여 진행 상황 공유, 코드 관리 그리고 conflict 발생할 떄 어떻게 대처할지 확인하였다.
- UI/UX를 사용자 친화적인 방향으로 최대한 생각하여 설계하는것이 부족했고 이 부분이 생각보다 중요함을 꺠달았다.
- 배포를 하지 않아 실제 개발된 코드 파일을 어떻게 배포 환경에 맞춰야 할지에 대한 부분을 확인하지 못해 아쉬웠다.
