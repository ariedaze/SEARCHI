# Clean Architecture and MVVM + RXSwift 연습

> 참고사항: `SEARCHI/Util/KakaoService-Info.plist` 의 `KAKAO_REST_API_KEY` 에 `REST API 키` 입력이 필요합니다!


### 고려사항

- [x] UISearchBar에 문자를 입력 후 1초가 지나면 자동으로 검색이 됩니다.
- [x] 검색어가 변경되면 목록 리셋 후 다시 데이터를 fetch 합니다.
  - [x] 데이터는 30개씩 페이징 처리합니다. 
  - [x] (최초 30개 데이터 fetch 후 스크롤 시 30개씩 추가 fetch)
- [x] 검색 결과 목록은 UICollectionView를 사용하여 3xN 그리드 모양으로 구성합니다. (각 아이템은 동일한 크기로 정사각형 형태) 
  - [x] 검색 결과가 없을 경우 '검색 결과가 없습니다.' 메시지를 화면에 보여줍니다.  
  - [x] 검색 결과 목록 중 하나를 탭 하였을 때 전체 화면으로 이미지를 보여줍니다. 
- [x] 전체 이미지 표시 할 때 좌우 여백이 0이고, 이미지 비율은 유지하도록 보여줍니다.
  - [x] 이미지가 세로로 길 경우 스크롤 됩니다. 
  - [x] response 데이터에 출처 'display_sitename', 문서 작성 시간 'datetime'이 있을 경우 전체 화면 이미지 밑에 표시해 줍니다.


### 아쉬운점

- 이전 검색 결과가 스크롤이 되어있는 상태에서 새로운 검색어를 입력했을 때 컬렉션뷰가 살짝 스크롤된 상태에서 새로운 데이터가 fetch되는 현상이 있습니다.
- datetime을 서버에서 온 그대로 출력하고 있습니다.


### 사용 라이브러리
- RxSwift
- RxCocoa
- Moya
- Moya/RxSwift
- Kingfisher
- Then
- Snapkit

