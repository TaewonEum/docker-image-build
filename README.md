# docker-image-build

파이썬 코드 도커 이미지 Build->docker hub에 업로드하는 과정


# requirements.txt 파일 생성

![image](https://user-images.githubusercontent.com/104436260/199645847-0db467b4-77eb-4d53-b17b-5b31a6971499.png)

 anaconda prompt 실행-> 이미지로 만들 파이썬 코드가 있는 폴더로 경로 변경-> pip list --format=freeze >./requirements.txt 입력
 
 
 ![image](https://user-images.githubusercontent.com/104436260/199646236-5fef0820-8222-465f-96c3-63641b4675c8.png)
 
 해당 경로 파일에 requirements.txt 파일 생성 확인
 
 # ipynb->py 파일 변환
 
 ![image](https://user-images.githubusercontent.com/104436260/199646597-0b15b82a-d637-4a70-9644-ef447f594556.png)
 
 jupyter nbconvert to script 파일명.ipynb 실행하여 py 파일로 변환
 
 # VS Code 실행
 
![image](https://user-images.githubusercontent.com/104436260/199646963-38f39ced-3cb6-4b9f-a950-8073083fe236.png)
 
 # Dokcerfile 생성 후 작성
 
 ![image](https://user-images.githubusercontent.com/104436260/199647900-3f31b7b3-c2c6-4fce-b787-99396a07d5dd.png)
 
 FROM python:3.7.13 -> 각자 파이썬 버전에 맞게 작성
 
 COPY . . -> host 환경의 파일 또는 디렉토리를 대상 컨테이너 이미지 안으로 복사한다.
 
 RUN pip install -r requirements.txt -> requirements.txt 안의 라이브러리 설치
 
 CMD ["python3", "source_code.py"] -> CMD 명령어는 RUN 명령어가 이미지를 빌드할 때 실행되는 것과 달리, 이미지로부터 컨테이너를 생성하여 최초로 실행할 때 수행됨.
 
 
 
 
