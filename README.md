# Handnote

직접 수기로 작성한 문서가 많아지게 되면 가지고 다니기 힘들뿐만 아니라, 관리하기도 불편하다. 

따라서 언제 어디서나 내가 필기한 문서를 관리할 수 있는 서비스의 필요성을 느끼게 되었다. 

이 서비스는 필기한 문서의 사진을 웹에 업로드하고, 이를 텍스트로 변환해 편집할 수 있는 서비스로, 직접 작성한 문서를 텍스트화 시키는 작업에 유용할 것으로 기대된다.

---------------------------------

## 기능

- 정리한 글의 이미지 → 텍스트

- 하이라이트된 글씨 → 텍스트

- 에디터

- 저장

-----------------------------------

## Architecture

### • 서비스 흐름도    

![handnote_architecture](https://user-images.githubusercontent.com/36119144/91645698-24118f00-ea82-11ea-8f14-52ce43a7ca30.png)

### • 이미지 인식 과정

![AI_Flow](https://user-images.githubusercontent.com/36119144/91645283-d21b3a00-ea7e-11ea-8227-a0565573323d.png)  

이미지를 단어별로 인식하여 단어정보가 담긴 데이터로 변환한다.

이 데이터를 CLOVA OCR을 통해 텍스트로 변환하고 줄번호와 글자크기의 정보를 담아 서버에 전송한다.



### • 하이라이트 부분 추출 과정

![hilight](https://user-images.githubusercontent.com/42924998/91671259-2ba76580-eb60-11ea-9092-dff144f6b30f.png)


-----------------------------------

## 구현 화면

![시작화면](https://user-images.githubusercontent.com/42924998/91634920-44642e00-ea2f-11ea-8c51-40cdce790b28.png)  


![로그인 후](https://user-images.githubusercontent.com/42924998/91634955-7d9c9e00-ea2f-11ea-9c49-f127f43786db.png)

▶  New Edit 버튼을 클릭하여 새로운 노트를 작성 ( 텍스트로 바꿀 이미지 필수)  


![스크린샷, 2020-08-31 08-04-10](https://user-images.githubusercontent.com/42924998/91671410-5fcf5600-eb61-11ea-8353-60a50d3aedd5.png)

▶  파입 업로드로 인식할 사진을 선택하고, **[텍스트로 변환]** 혹은 **[중요부분 변환]** 버튼을 누르면 인식한 글씨가 텍스트창에 들어가게 됌.  

![스크린샷, 2020-08-31 08-04-55](https://user-images.githubusercontent.com/42924998/91671439-ac1a9600-eb61-11ea-96de-891fa2399b6f.png)

빨강색 테두리 - 변환 중  |   파랑색 테두리 - 변환 완료    |   초록색 테두리 - 선택한 이미지(Preview)

![스크린샷, 2020-08-31 08-06-41](https://user-images.githubusercontent.com/42924998/91671419-7d9cbb00-eb61-11ea-9a96-8409ff9d6e2e.png)

**[텍스트로 변환]** - 이미지의 모든 글씨 인식

![스크린샷, 2020-08-31 08-08-14](https://user-images.githubusercontent.com/42924998/91671428-94dba880-eb61-11ea-82d3-21bf079aca48.png)

**[중요부분 변환]** - 이미지의 하이라이트한 글씨만 인식  
  
Link: http://3.34.203.63:8080/

--------------------------------------

## 도커

`docker-compose up`

--------------------------------------

## Contact Us

정현수 <mses1572@naver.com>

이지헌 <dlwlgjs132@naver.com>

임도연 <dodocat52@naver.com>
