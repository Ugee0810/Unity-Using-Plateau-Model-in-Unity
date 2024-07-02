## What is Plateau SDK for Unity ?
![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/56688021-69f7-4de3-81d4-d92ea551de01)

[PLATEAU SDK for Unity란?](https://www.mlit.go.jp/plateau/learning/tpc17-1/#p17_1)

Plateau SDK는 일본의 3D 도시 모델 플랫폼인 PLATEAU의 데이터를 Unity 환경에서 사용할 수 있게 해주는 도구입니다.
이를 통해 개발자들은 현실감 있는 3D 도시 모델을 활용한 다양한 애플리케이션과 게임을 쉽게 제작할 수 있습니다.

무엇을 배울 수 있나요？
- 公開されている都市や各市町村のデータの簡単な内容の説明とその入手の方法
- Unityに3Dモデルをインポートする方法
- インポートした重い3Dモデルを最適化して描写パフォーマンスを何十倍も上げる方法
- Unityでフライスルー（飛べる）

### 주요 기능
![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/0c2e0fd1-9ca3-49b8-add1-8782631d6593)

1. **3D 도시 모델 데이터 로드** : PLATEAU 플랫폼에서 제공하는 고해상도 3D 도시 모델 데이터를 Unity로 가져와 사용할 수 있습니다.
2. **지형 및 건물 렌더링** : 실제 지형과 건물 데이터를 기반으로 한 고품질의 렌더링을 지원합니다.
3. **경로 탐색 및 시뮬레이션** : 도시 내에서의 경로 탐색과 다양한 시뮬레이션을 구현할 수 있는 기능을 제공합니다.
4. **커스터마이징** : Unity의 풍부한 기능을 활용하여 3D 도시 모델을 사용자 요구에 맞게 커스터마이징할 수 있습니다.
5. **통합 및 확장성** : 다른 시스템 및 API와의 통합이 용이하며, 확장 가능한 구조를 가지고 있습니다.

#### CityGML 형식이란?
CityGML 형식은 도시 및 지리 정보를 3차원으로 표현하기 위해 사용되는 XML 기반의 오픈 표준 형식입니다. Open Geospatial Consortium (OGC)에서 개발한 이 표준은 도시의 다양한 요소들을 모델링하고 시각화할 수 있도록 설계되었습니다. 이 형식은 건물, 교통 인프라, 토지 이용, 식생, 수역 등 도시 환경을 구성하는 다양한 객체들을 3D로 표현할 수 있게 해줍니다.

주요 특징
- **다중 해상도(Level of Detail, LOD)** : 다중 해상도를 지원하여 다양한 상세 수준의 도시 모델을 만들 수 있습니다. LOD1은 단순한 블록형 모델, LOD2는 지붕 모양을 포함한 모델, LOD3는 외부 디테일이 더 추가된 모델, LOD4는 내부 구조까지 포함하는 모델을 의미합니다.
- **주제별 모델링(Feature-Based Modeling)** : 건물, 교통망, 토지 이용, 지형, 식생 등 다양한 주제별 클래스를 통해 도시 객체를 모델링합니다. 각 클래스는 그에 해당하는 속성과 기하학적 정보를 가집니다.
- **속성 및 관계(Attribute and Relationship)** : CityGML 객체는 속성(예: 건물의 높이, 용도 등)과 다른 객체와의 관계(예: 건물이 위치한 구역, 도로와의 연결 등)를 포함할 수 있습니다. 이를 통해 보다 현실적이고 유의미한 도시 모델을 만들 수 있습니다.
- **확장 가능성(Extensibility)** : 사용자 정의 확장을 허용하여 특정 응용 분야의 요구를 충족할 수 있습니다. 예를 들어, 에너지 소비 분석, 소음 모델링 등의 특정 목적을 위한 확장을 추가할 수 있습니다.
- **상호 운용성(Interoperability)** : 다른 GIS 및 3D 시각화 소프트웨어와 호환성을 유지하며, 다양한 애플리케이션에서 도시 데이터를 효율적으로 활용할 수 있게 해줍니다.

### CityGML 형식은 Plateau SDK외에도 Unity에서 일반적으로 사용가능한가요?
CityGML 형식은 기본적으로 GIS 및 3D 도시 모델링을 위한 형식으로, Unity와 같은 게임 엔진에서 직접적으로 사용하는 것은 일반적이지 않습니다. 그러나 CityGML 데이터를 Unity에서 사용하기 위해 몇 가지 방법이 있습니다.

1. **CityGML 변환 툴 사용** : CityGML 데이터를 Unity에서 사용하기 위해 먼저 다른 형식으로 변환해야 합니다. 예를 들어, CityGML 데이터를 COLLADA(.dae), FBX, OBJ 등 Unity에서 지원하는 3D 모델 형식으로 변환할 수 있습니다. 이를 위해 다양한 변환 도구나 소프트웨어를 사용할 수 있습니다. 대표적인 변환 도구로는 FME(Feature Manipulation Engine), 3DCityDB Importer/Exporter 등이 있습니다.
2. **전용 플러그인 및 SDK** : Unity에서는 CityGML 데이터를 다룰 수 있도록 도와주는 전용 플러그인이나 SDK를 사용할 수 있습니다. 예를 들어, 일부 GIS 소프트웨어 회사에서 제공하는 Unity용 GIS SDK를 사용하면 CityGML 데이터를 쉽게 Unity 프로젝트에 통합할 수 있습니다. Cesium for Unity와 같은 플러그인은 3D 타일링된 지리 데이터를 Unity에서 사용할 수 있게 해줍니다.
3. **자체 스크립트 작성** : CityGML 파일을 파싱하고 Unity의 GameObject로 변환하는 자체 스크립트를 작성할 수도 있습니다. 이를 위해서는 CityGML 파일을 XML로 파싱하고, 각 객체를 Unity의 적절한 형식으로 변환하는 과정이 필요합니다. 이 방법은 많은 시간이 소요될 수 있지만, 특정 요구에 맞게 데이터를 처리할 수 있다는 장점이 있습니다.

이번 문서에선 CityGML 변환 툴 중 하나인 PLATEAU SDK를 사용합니다.

## Using Plateau Model in Unity
### 작업 환경
- MacOS
- Unity Editor Version 6000.0.5f1 Silicon
- Universal RP 17.0.3
- Plateau SDK for Unity 2.3.2 [(Releases](https://github.com/Project-PLATEAU/PLATEAU-SDK-for-Unity/releases))

### Install Plateau SDK for Unity
![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/13c29472-4194-478c-ba9b-01656d1111d6)
![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/01279e29-8eeb-4228-b28a-e07aa55ec94a)
다운로드한 Plateau SDK for Unity 2.3.2를 압축 해제하여 Project/Packages 경로에 넣어줍니다.

### Plateau 3D모델 다운로드(로컬 데이터를 사용하는 경우)
[3D都市モデル(Project PLATEAU)ポータルサイト](https://www.geospatial.jp/ckan/dataset/plateau)에 가서 불러올 도시를 선택합니다.
- 다양한 포맷을 지원하지만 Unity에 직접 Import할 수 있는 FBX형식 모델을 다운로드합니다.
- ![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/9ff0fd3a-1440-4a92-b7c2-155a5a0f20c5)
  - 위 사진처럼 특정 도시의 최신 데이터는 FBX는 제공하지 않아 PLATEAU SDK를 사용하여 변환하는 작업이 별도로 필요할 수 있습니다. 따라서 CityGML형식을 다운로드하여 [Plateau SDK Installation](https://project-plateau.github.io/PLATEAU-SDK-for-Unity/manual/Installation.html)절차를 진행한 뒤 FBX로 변환합니다.
  - PLATEAU SDK는 v2 이상을 지원합니다.
  - ![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/1ade4593-89aa-43db-8f4a-11e1757181dd)

본 문서에서는 名古屋市（2022年度）도시를 기준으로 진행합니다.

### Unity에 3D 모델링 임포트하기
#### 로컬 가져오기

#### 서버 가져오기

## Reference
- [jhorikawa_err - Using Plateau Model in Unity - UnityにPlateauモデルを持っていこう](https://qiita.com/jhorikawa_err/items/a8562b5d38bb6ae3edea)
- [PLATEAU SDK for Unity Manual](https://project-plateau.github.io/PLATEAU-SDK-for-Unity/index.html)
