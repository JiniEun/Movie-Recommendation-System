# Movie-Recommendation-System
Build a Movie Recommendation System using Python

MovieShelf 영화 검색 웹페이지 프로젝트에 적용해보고자 영화 추천 알고리즘 코딩

Python - Colab 이용

> Colab이란?
> 구글 코랩(Colab)은 클라우드 기반의 무료 Jupyter Notebook 개발 환경이다. <br>
> 내부적으로는 코랩 + 구글드라이브 + 도커 + 리눅스 + 구글클라우드의 기술스택으로 이루어진 것으로 알려져있다.


<br>

## 1. data set - Kaggle 

### 구글 드라이브에 업로드하고 불러오기

Colab이 구글에서 제공하는 서비스라 파일 이용시 구글 드라이브의 자료를 불러오는 것이 편하다. <br>

<img src="https://user-images.githubusercontent.com/49184115/160849484-5856f6f1-fdbf-43ad-9a10-b47fc671de78.png" width="40%" height=auto/>

![image](https://user-images.githubusercontent.com/49184115/160848263-af193b9b-933e-4c94-aabc-f4aab2fb7ca3.png)

화면 좌측에 그림과 같은 폴더모양을 누르고 드라이브 마운트를 클릭하면 자동으로 실행할 코드가 입력된다. <br>

```python
from google.colab import drive
drive.mount('/content/drive')
```

![image](https://user-images.githubusercontent.com/49184115/160848802-e3f91793-ae69-46fe-b974-39967bc2c641.png)

코드를 실행하고 구글 계정에 로그인 화면이 등장하면 로그인을 진행한다.
드라이브 업로드한 데이터를 찾고 경로를 복사하여 pd.read 형식으로 불러오면 된다.
불러올 데이터를 우클릭하거나 오른쪽 점점점 버튼을 누르면 경로 복사가 가능하다.


### Kaggle Dataset 
이용한 Kaggle Dataset
https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset?datasetId=3405&searchQuery=kmeans&select=ratings.csv

movies_metadata.csv, credits.csv, keywords.csv

## Data 처리

