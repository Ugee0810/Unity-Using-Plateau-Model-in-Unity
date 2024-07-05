## What is Plateau SDK for Unity ?
![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/56688021-69f7-4de3-81d4-d92ea551de01)

[PLATEAU SDK for Unity란?](https://www.mlit.go.jp/plateau/learning/tpc17-1/#p17_1)

Plateau SDK는 일본의 3D 도시 모델 플랫폼인 PLATEAU의 데이터를 Unity 환경에서 사용할 수 있게 해주는 도구입니다.
이를 통해 개발자들은 현실감 있는 3D 도시 모델을 활용한 다양한 애플리케이션과 게임을 쉽게 제작할 수 있습니다.

[Plateau SDK 사용 사례](https://www.mlit.go.jp/plateau/use-case/)

### 샘플 프로젝트
- [2024년 GIS 샘플](https://github.com/Project-PLATEAU/PLATEAU-SDK-for-Unity-GISSample)
  - 도시 정보를 보여주는 샘플입니다.
  - ![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/5b82e3da-016b-4597-8933-51b9b8c4ed55)
- [2024년 게임 샘플](https://github.com/Project-PLATEAU/PLATEAU-SDK-for-Unity-GameSample)
  - 도시를 무대로 이동하는 게임 샘플입니다.
  - ![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/9e2db2b2-cf28-473f-b75d-7656af7f9207)

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
- 만약 도심 내부의 특정 지역만을 다운로드 하고 싶다면 지역 메쉬 코드(위도, 경도)의 범위 다이어그램을 확인하고 해당 번호의 FBX형식으로 파일을 다운로드합니다.
  - ![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/b2df5e16-6dd4-47c5-8f82-7db4a54e8293)
  - ![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/69dc45bd-c74b-4596-9120-e0ca7c571e30)
  - ![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/424f1d0d-c6ed-4836-98d4-ce8eb4259129)

### Unity에 3D 모델링 임포트하기
#### Only MacOS Issue
1. MacOS에서 악성 소프트웨어 문구가 나올 경우
2. 설정 - 개인 정보 보호 및 보안 - 보안 설정 - **"libplateau.dylib" 파일에 대한 허용**
3. 정상 동작 확인

![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/76d78a37-ff4c-4e96-8cfc-aa7b8076eb83)
![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/75dda029-e188-4bb4-8625-1fc1f8e0b339)
![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/d3ccc35b-2a81-49e4-a3d1-7b090c043125)

#### 로컬에서 가져오기
다운로드한 FBX를 Assets의 임의의 루트에 넣고 Scene으로 넣어줍니다.
![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/5a111555-9ff0-40de-9534-32dbbf8db2fe)

가져온 모델을 장면으로 드래그하면 환경에 따라 텍스처가 가져오지 않을 수 있습니다. 그 때는 메쉬 애셋의 Materials 탭에서 Extract Textures 버튼을 눌러 원하는 폴더에 텍스처를 내보냅니다. 그러면 자동으로 메쉬에 텍스처가 붙여집니다.
![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/628bbe1c-60c6-4318-9b26-25c0cb29dd28)
![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/76c0e8de-43ba-4b51-bfc6-883658d70afb)

#### 서버에서 가져오기
1. Unity 상단 탭에서 PLATEAU SDK Open
2. インポート元에서 サーバー(서버)로 선택
3. データセットの選択(데이터 설정 선택)에서 都道府県(도도부현)에서 추가할 지역 선택 -> データセット(데이터 설정)에서 해당 지역 도시 선택
4. 아래 쪽 基本座標系(기본좌표계)를 선택한 데이터 설정과 가까운 곳으로 설정
5. 이후 아래 쪽 範囲選択(범위 선택)으로 결정
<img width="994" alt="image" src="https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/52c742ca-5c88-4a78-a1e8-97c8c851da39">

6. Scene View로 이동

![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/6f6ecbc8-ea49-4386-b427-dccec5c3f4ca)
![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/539e601f-fc5c-4446-904e-89475b30d78b)

- 전부 선택 해제
- 결정
- 메쉬 코드 검색
- 취소(다시 5번 절차로)

7. 추가할 범위 지정 후 결정

![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/f37a010a-9026-4c27-a932-6c7bd75293fd)

8. 결정하면 PLATEAU SDK 탭에서 3번 地物別設定(지형별 설정)이 열리게 됩니다. 이는 지형의 종류에 구분하여 임포트할 것을 선택하는 설정입니다. 여기서 중요한 설정만 우선 설명합니다.

- 一般設定(일반 설정)
  - テクスチャを含める(텍스처 포함 여부)
  - テクスチャを結合する(텍스처 결합 여부)
  - Mesh Colliderをセットする(메쉬 콜라이더 설정 여부)
  - モデル結合(모델링 결합)
    - 최소 지형 단위(벽면)
    - 주요 지형 단위(건축물, 도로 등)
    - 지역 단위
  - 属性情報を含める(속성 정보 포함)

![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/4161daf9-8163-4fd0-9a3a-7b7238a440a5)

9. モデルをインポートする(모델링 임포트하기) 선택
10. 아래부터 다운로드가 진행됩니다.

![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/f414dba3-d245-407f-babe-515e355e91f0)

11. Game, Scene View에서 확인합니다.

![image](https://github.com/Ugee0810/Unity-Using-Plateau-Model-in-Unity/assets/85896566/135f53bb-0a21-4e9e-8bd5-f34077fa1786)

## Reference
- [jhorikawa_err - Using Plateau Model in Unity - UnityにPlateauモデルを持っていこう](https://qiita.com/jhorikawa_err/items/a8562b5d38bb6ae3edea)
- [PLATEAU SDK for Unity Manual](https://project-plateau.github.io/PLATEAU-SDK-for-Unity/index.html)
