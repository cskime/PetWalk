
Pet Walk

- 

Description

- 반려동물과 산책하면서 주인도 재미를 느낄 수 있도록 주어진 산책 지점을 찍고 오면 보상을 받을 수 있는 앱
- 기능 보완을 거쳐 추후 앱스토어 출시 예정

Tech Stack



Firebase

- Cloud Firestore를 사용하여 반려동물 정보 및 산책 기록 데이터 관리
- Cloud Storage에 이미지를 저장하고 url을 데이터베이스에 저장

UIView Animation

- UIView.animate()으로 animation 구현
- UIView.animateKeyFrames()을 사용하여 여러 동작의 연속적인 animation 구현

MapKit

- CoreLocation을 활용하여 사용자 위치 tracking
- 위경도 좌표를 이용한 실제 거리 측정 및 MKAnnotation 및 MKAnnotationView을 활용한 위치 정보 시각화

Architecture Design

- MVC Pattern을 적용한 class design

Part

Database

- 데이터 구조 설계 및 Cloud Firestore, Cloud Storage를 이용한 데이터베이스 관리

MapKit

- CoreLocation을 사용한 



- Tech Stack : Firebase, MVC Pattern, Singleton Pattern, MapKit, UIView Animation
- Part : Firebase, Design Pattern, MapKit
  - Firebase
    - 사용자 및 반려동물 정보와 산책 정보 저장을 위해 Firebase의 Cloud Firestore을 사용하고, 이미지 저장에 Firebase Cloud Storage 사용
    - Firestore는 `Collection-Document 데이터 구조 및 Document가 하위 Collection을 갖는 구조이기 때문에, 하나의 Pet object가 여러 개의 Walk object를 가져야 하는 데이터 구조를 쉽게 표현하기에 적합
      <img src="" alt="Data Architecture" width="50%">
  - Design Pattern
    - MVC : MVC Pattern을 적용하여 프로젝트의 유지보수 효율을 높임 
      <img src="" alt="MVC Pattern Architecture" width="50%">
    - Singleton : Database에 반려동물 및 산책 기록 데이터에 대한 요청을 줄이기 위해 별도의 메모리에 캐싱(caching)해서 사용하고, singleton pattern을 적용하여 프로젝트 전체에서 공통으로 접근할 수 있도록 함
      <img src="" alt="Singleton and Caching Data" width="50%">
  - MapKit : CoreLocation과 MKMapView를 활용하여 사용자의 위치를 추적하고 목표 지점과의 거리(m)를 측정하여 목표 지점에 도달했는지 확인
- Learn : 해커톤을 통해 새롭게 배운 것들
  - 







Education

What's New

- [Date Class]()
- [Cloud Firestore]()
- [UIView Animation]()