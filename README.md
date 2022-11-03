# docker-image-build

파이썬 코드 도커 이미지 Build->docker hub에 업로드하는 과정


# requirements.txt 파일 생성

![image](https://user-images.githubusercontent.com/104436260/199645847-0db467b4-77eb-4d53-b17b-5b31a6971499.png)

 실행-> 이미지로 만들 파이썬 코드가 있는 폴더로 경로 변경-> pip list --format=freeze >./requirements.txt 입력
 
 ![image](https://user-images.githubusercontent.com/104436260/199646236-5fef0820-8222-465f-96c3-63641b4675c8.png)
 
 해당 경로 파일에 requirements.txt 파일 생성 확인
 
 # ipynb->py 파일 변환
 
 ![image](https://user-images.githubusercontent.com/104436260/199646597-0b15b82a-d637-4a70-9644-ef447f594556.png)
 
 jupyter nbconvert to script 파일명.ipynb 실행하여 py 파일로 변환
