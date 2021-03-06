# 클라우드 컴퓨팅의 소개
## 클라우드 컴퓨팅 정의
컴퓨팅 파워, 데이터베이스, 스토리지, 애플리케이션 및 기타 **IT 리소스들을 온디맨드로 인터넷을 통해 제공하고 
사용한 만큼만 비용을 지불**하는 것을 의미한다. 이러한 리소스들은 전세계적으로 여러곳에 위치한 대규모 데이터센터에 구축된 서버컴퓨터에서 실행된다.  

온디맨드 : '요구만 있으면 (언제든지)'~ 즉, 공급 중심이 아니라 수요가 모든 것을 결정하는 시스템이나 전략 등을 총칭

## 소프트웨어로써의 인프라
클라우드 컴퓨팅을 사용하면 더이상 인프라를 하드웨어가 아닌 소프트웨어로 생각하고 사용할 수 있다.
기존 하드웨어 방식의 인프라를 구축할 경우 물리적 비용(공간, 보안, 인력, 용량 - 스토리지의 최대 피크를 추정하여 용량을 provisioning 해야함. 등)이 소모된다.  

반면에 소프트웨어 방식의 인프라를 구축하면 이러한 물리적 한계를 극복할 수 있다. 소프트웨어 인프라는 하드웨어 인프라에 비해 상대적으로 유연하고, 간편하고 빠르게 변경이 가능하다. 
이를테면, 하드웨어 서버 장비를 이동시키는 것과 소프트웨어 서버의 물리적인 위치를 바꾸는 것, 정적인 스토리지 할당과 동적인 스토리지 할당.  

## 클라우드 서비스 모델
다음 클라우드 서비스 모델은 IT 리소스 제어 능력을 높은 순에서 낮은 순으로 나열한다.
1. IaaS (서비스형 인프라)  
   최고수준의 유연성과 제어기능을 제공하는 모델이다. 이를테면, 네트워킹 기능과 가상 컴퓨터에 대한 액세스, 스토리지를 제공한다.  
   ex) 아예 가상의 컴퓨터 한대를 제공해 준다고 생각하면 편하다..  
   

2. PaaS (서비스형 플랫폼)  
   일반적으로 하드웨어나 운영체제와 관련이 있다. 자동화 기능을 통해 관리되므로 프로비저닝 작업이 아니라 애플리케이션을 통해 배포하고 관리하는데 집중할 수 있다.  
   
   
3. SaaS (서비스형 소프트웨어)  
   서비스 공급자에의해 실행되고 관리되는 완전한 제품을 고객에게 제공한다. 대부분의 경우 서비스형 소프트웨어는 최종 사용자 애플리케이션을 지칭한다.  
   ex) 넷플릭스, colab, google docs, google sheet ..


4. FaaS

## 클라우드 컴퓨팅 배포 모델
애플리케이션을 배포할 수 있는 환경을 의미한다.
1. 클라우드 (퍼블릭 클라우드)  
   클라우드 기반 애플리케이션은 모든 구성요소가 클라우드에 배포되는 구현 유형으로 클라우드에 완전히 배포된다.
   애플리케이션의 모든 부분이 클라우드에서 실행된다. 클라우드 기반 애플리케이션은 클라우드에서 생성되거나 기존 인프라에서 클라우드로 마이그레이션된 경우이다.  
   

2. 하이브리드  
   기존 인프라와 애플리케이션을 클라우드 기반 리소스에 연결하는 방식으로 배포된다. 즉, 클라우드에 존재하지 않고 물리적 시설에 존재한다.
   하이브리드 모델의 일반적인 배포 방식은 클라우드와 기존 온프레미스 사이에 배포하는 것이다. 이렇게 하면 클라우드 리소스를 내부 시스템에 연결하는 동시에 구현 환경이 확장된다.  
   

3. 온프레미스 (프라이빗 클라우드)  
   가상화 및 리소스 관리도구를 사용하여 온프레미스에 리소스를 배포하는 것을 프라이빗 클라우드라고 부른다.

## AWS와 기존 IT의 유사
<img width="918" alt="image" src="https://user-images.githubusercontent.com/32003817/110233237-027bed80-7f66-11eb-8d2f-792c55c34576.png">

* 보안그룹은 방화벽(firewall)에 해당한다.
* 네트워크 ACL 은 ACL (Access Control List)에 해당한다.
* IAM(Identity and Access Management)은 사용자 프로비저닝과 유사하다.
* Elastic Load Balancing 과 Amazon Virtual Private Cloud는 라우터, 네트워크 파이프라인, 스위치에 해당한다.
* AMI(Amazon Machine Image는 Amazon EC2 instance를 초기화하는데 사용되며 이는 온프레미스 서버와 비슷한 역할을 한다.  
* DAS (Direct Attached Storage) = Amazon EBS (Elastic Block Store)
* Amazon EFS (Elastic File System) 은 가상머신에도 연결되지만 전통적인 SAN (Storage Area Network) 에 해당한다.
* Amazon S3 (Simple Storage Service) 는 인터넷을 통해 파일을 저장할 수 있는 기능을 제공하며 NAS (Network Attached Storage)에 해당한다.
* Amazon RDS (Relational Database Service) RDBMS (Relational DataBase Management System)에 해당한다.

# 클라우드 컴퓨팅의 이점
1. 자본비용을 가변비용으로 대체한다.  
리소스를 사용할때만, 사용한 리소스만큼만 동적으로 비용을 지불하는 장점이 있다.
   
2. 거대한 규모의 경제  
고객의 사용량이 누적됨에 따라 AWS는 높은 규모의 경제를 달성하고 고객들에게 지불해야하는 요금을 낮추어 혜택으로써 돌려준다.
   
3. 용량 추정 불필요  
클라우드 사용량에 따라 동적으로 용량을 할당할 수 있다.
   
4. 속도 및 민첩성 향상
기존 인프라를 사용할 경우 물리적 한계로 인해 인프라를 구축하는데에 오랜 시간이 소요되지만 AWS를 사용하면 클릭 단 한번으로 IT 리소스를 할당받을 수 있다.
   
5. 데이터 센터 유지 및 운영 관리에 대한 비용 투자 불필요
6. 몇 분만에 애플리케이션을 전세계로 배포

# AWS (Amazon Web Service) 소개
## 웹 서비스란?
인터넷을 통해 이용할 수 있는 소프트웨어로 API (Application Programming Interface)를 통해 상호작용 하며,
JSON이나 XML과 같은 표준화된 형식을 사용한다.

## AWS란?
* AWS는 다양한 글로벌 클라우드 기반 제품을 제공하는 안전한 클라우드 플랫폼이다.
* AWS는 컴퓨팅, 스토리지, 네트워크, 데이터베이 및 기타 IT 리소스와 관리도구에 대한 온디맨드 액세스를 제공한다.
* AWS는 유연성을 제공한다. (필요에 따라 일시적 혹은 영구적으로 정지할 수 있다.)
* 필요한 개별서비스에 대해 사용한 만큼만 비용을 지불하면 된다.
* AWS 서비스는 빌딩블록처럼 유기적으로 작동한다. (데이지 체인 방식)

## 서비스 선택
* **Amazon EC2** : 컴퓨팅 측면에서 AWS 컴퓨팅 리소스와 인프라를 완벽하게 제어하려는 경우
* **Amazon Lambda** : 코드를 실행하면서 서버를 관리하거나 프로비저닝하지 않으려하는 경우 
* **Amazon Elastic Beanstalk** : 사용하면 서비스를 프로비저닝하여 웹 애플리케이션을 자동으로 배포 관리 및 확장
* **Amazon Lightsail** : 간단한 웹 애플리케이션을 위한 플랫폼, 간단한 방법으로 웹 애플리케이션을 시작하려고 할 때 사용
* **AWS Batch** : 수십만개의 배치 워크로드를 안정적으로 실행해야 할 때 사용
* **AWS Outposts** : 온프레미스 데이터 센터에서 AWS 인프라를 실행하고자 할 때 사용
* **Amazon Elastic Container Service, Amazon Elastic Kubernetes, AWS Fargate** : 컨테이너 또는 마이크로서비스 아키텍쳐를 구현하려고 하는 경우 사용
* **VMware Cloud on AWS** : 온프레미스 서버 가상화 플랫폼을 AWS로 마이그레이션하려는 경우

## AWS 상호작용 방법
1. AWS Management Console  
   사용하기 쉬운 그래픽 유저 인터페이스

   
2. AWS CLI (Command Line Interface)  
   개발 명령 또는 스크립트를 사용하여 서비스에 액세스
   

3. SDK  
   코드에서 직접 액세스 (패키지 제공)
   
세 가지 방법 결국에는 모두 **REST API** 기반이다.

## AWS CAF (Cloud Adoption Framework)
AWS CAF는 조직이 전사적으로, 또한 IT 수명 주기 전반에 걸쳐 클라우드 컴퓨팅에 대한 포괄적인
접근 방식을 구축하여 성공적인 클라우드 도입을 가속화하는데 도움이 되는 지침과 모범 사례를 제공한다.  

AWS CAF는 6가지 관점으로 구성되어 있다. 각 관점은 인력, 프로세스, 기술에 적용된다.  

아래 3가지 관점은 비즈니스 역량에 집중된 관점
* Business (IT 재무, IT 전략, 이점 실현, 비즈니스 위험 관리)  
  비즈니스 관리자, 재무 관리자, 예산 소유자 및 전략 이해 관계자 :  
  IT가 비즈니스 요구사항에 부합하는지,
  그리고 IT 투자를 추적하여 비즈니스 성과를 입증할 수 있는지 확인해야 한다.  
  -> 설득력 있는 클라우드 도입의 타당성을 확보  

* People (리소스 관리, 인센티브 관리, 경력 관리, 교육 관리, 조직 변화 관리)  
  인사, 인력 배치 및 인력 관리자 :  
  민첩한 조직을 구축하려면 교육, 인력 배치 및 조직 변화에 중점을 두어야 한다.  
  -> AWS CAF를 사용하여 조직의 구조 및 역할, 새로운 기술 및 프로세스 요구사항을 평가하고 그 격차를 파악할 수 있다.
  요구사항과 격차를 파악하면 민첩한 조직을 구축하기 위한 교육 인력 배치 및 조직 변경의 우선순위를 정하는데 도움이 된다.  

* Governance (포트폴리오 관리, 프로그램 및 프로젝트 관리, 비즈니스 성과 관리, 라이선스 관리)  
  CIO(최고 정보 책임자), 프로그램 관리자, 엔터프라이즈 아키텍트, 비즈니스 분석가 및 포트폴리오 관리자 :  
  조직은 IT 투자의 비즈니스 가치를 극대화하고 비즈니스 위험을 최소화할 수 있도록 
  IT 전략 및 목표와 비즈니스 전략 및 목표에 맞추어 기술을 확보하고 프로세스를 구축해야 한다.  
  -> AWS CAF를 사용하여 IT 전략 및 목표를 비즈니스 전략 및 목표에 맞추는 데 필요한 기술과 프로세스에 집중할 수 있다.
  

아래 3가지 관점은 기술 역량에 집중된 관점
* Platform (컴퓨터 프로비저닝, 네트워크 프로비저닝, 스토리지 프로비저닝, 데이터베이스 프로비저닝, 시스템 및 솔루션 아키텍처, 애플리케이션 개발)  
  CTO, IT 관리자 및 솔루션스 아키텍트 :  
  IT 시스템의 특성과 그 관계를 이해하고 전달해야 한다. 대상 상태 환경의 아키텍처를 자세히 설명할 수 있어야 한다.  
  
* Security (자격증명 및 액세스관리, 탐지제어, 인프라보안, 데이터보호, 인시던트 대응)  
  CISO, IT 보안 관리자 및 IT 보안 분석가 :  
  조직이 보안 목표를 충족하는지 확인해야 한다.  
  
* Operations (서비스 모니터링, 애플리케이션 성능 모니터링, 리소스 인벤토리 관리, 릴리스 관리 / 변경 관리, 보고 및 분석, 비즈니스 연속성 / 재해 복구, IT 서비스 카탈로그)  
IT 운영 관리자 및 IT 지원 관리자 :  
  비즈니스 운영과 연계하고 지원하며 일일, 분기별, 연도별로 비즈니스 수행 방식을 정의한다.

