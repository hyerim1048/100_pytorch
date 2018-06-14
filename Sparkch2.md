RDD 탄력적 분산 데이터셋
클러스터의 여러 노드에 분산할 수 있는 객체들의 컬렉션

- 스파크에서는
- spark context를 통해서 외부 데이터로 부터 RDD 생성
- 이미 만들어진 RDD를 가공해서 RDD 생성 (join, filter…)

 sc.parallelize(array,숫자: 파티션 수) : 데이터를 RDD로 만듬

이 단계까지는 메모리에 데이터 안올라감

- 스파크는 대화형 쉘 말고 컴파일된 애플리케이션 형태도 지원하는데 컴파일과 의존성 관리를 위해서 메이븐을 주로 사용. 예제 저장소 확인
simplesparkproject/
