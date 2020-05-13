# Linux에 Kaggle API 설치 및 사용

[참고 포스트]( https://paiai.tistory.com/30 )

[공식 문서 링크]( https://github.com/Kaggle/kaggle-api )



### 1. [Kaggle 사이트]( https://www.kaggle.com/ ) 접속 후 kaggle.json파일 받기

- [Kaggle 사이트]( https://www.kaggle.com/ )접속
- My Account
- Create API Token
- kaggle.json파일 다운완료



### 2. Kaggle API 설치 과정

- Kaggle API 설치

  `pip install kaggle --upgrade`

- 설치 확인

  `pip show kaggle`

- Kaggle API가 설치된 위치 확인

  `kaggle config path`

- kaggle.json 파일을 이동

  `mv kaggle.json [kaggle config path시 나온 path]`

- 권한 설정

  `chmod 600 [kaggle config path시 나온 path]/kaggle.json`

\### 만약 .kaggle 폴더가 안 보일 경우 `ls -a`를 사용하여 확인하고 없을시 다시 설치



### 3. Kaggle API 간단한 commands

- ```
  kaggle competitions {list, files, download, submit, submissions}
  ```

- ```
  kaggle datasets {list, files, download}
  ```

- ```
  kaggle config {path}
  ```



### 4. Kaggle API를 통해 dataset다운 받아 보기

예제) [dstl satellite imagery feature detection]( https://www.kaggle.com/c/dstl-satellite-imagery-feature-detection )

- 대회 검색

```
kaggle competitions list -s dstl
```

```
### 결과 ###
ref                                       deadline             category    reward  teamCount  userHasEntered  
----------------------------------------  -------------------  --------  --------  ---------  --------------  
dstl-satellite-imagery-feature-detection  2017-03-07 23:59:00  Featured  $100,000        419            True 
```



- 대회 dataset 다운 받기

  - 기본으로 설정된 경로로 다운 받는 법

    default 경로 : ~/.kaggle/competitions/dstl-satellite-imegery-feature-detection

    ```
    kaggle competitions download -c dstl-satellite-imagery-feature-detection
    ```

  - 다른 경로 지정해서 다운 받는 법

    예시 경로: ~/satellite/dataset/dstl

    ```
    kaggle competitions download -c dstl-satellite-imagery-feature-detection -p ~/satellite/dataset/dstl
    ```

    

