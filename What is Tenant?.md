## 🏛 What is Tenant?
Office 365 조직을 위해 사용되는 용어<br>
테넌트는 당신의 조직을 위한 것으로 조직과 자산을 위한 샌드박스 환경(보안 소프트웨어 환경)<br>
테넌트는 O365 데이터 센터 전반에 걸쳐 속해있고 조직의 사용자들, 도메인, 구독 등등의 아이템들을 위한 컨테이너<br><br>

### If you create Tenant, 🥳
당신이 조직을 위한 테넌트를 생성하면, 2개의 다른 DNS 엔트리(DNS entries)를 디폴트로 등록한다. <br>
이 시점에서 추가한 사용자들은 누구나 자동으로 user@tenantname.onmicrosoft.com 형식의 로그인/이메일 주소를 갖게 된다.<br>
테넌트 자체를 갖는 것은 비용이 들지 않는다. 당신의 테넌트를 위해 당신이 구독한 게 어떤 것인지와 당신이 지불하고 있는 라이선스의 수에 따라 비용이 발생한다. <br>
(O365 구독, Sharepoint online, Exchange, Power bi etc.)<br>
##### (cf. DNS, Domain Name System : 사람이 읽을 수 있는 도메인 이름을 컴퓨터가 읽을 수 있는 IP주소로 변환(www.amazom.com → 192.0.2.44)<br>ref.https://aws.amazon.com/ko/route53/what-is-dns/)
<br>

#### SaaS는 Multi-tenant 가능 
(https://digitalguardian.com/blog/saas-single-tenant-vs-multi-tenant-whats-difference)
-Multi-tenancy : 하나의 애플리케이션을 다수의 고객(tenant)이 공유하여 사용하는 다중 소유가 가능한 아키텍처, 하나의 인스턴스를 통해 다양한 요구사항을 가진 고객을 지원하므로 유지보수 비용이 절감되고 규모의 경제 달성 가능
각 회사가 SaaS에서 tenant 영역을 가지는 것이 SaaS에 가입하는 것
tenant의 관리자가 데이터를 관리(사용범위 관리)
-tenant 생성 : 테스트용 데모 tenant(enterprise with users no content용)
생성 사이트 cdx.transform.microsoft.com
여기서 my environments에서 생성된 테넌트 계정 확인 가능
시크릿 창을 통해 이 계정으로 admin.microsoft.com에 로그인하면 나의 user들 확인 가능
enterprise : 대기업용, business : 중소기업용
MS의 data center는 전세계 여러 국가에 분포, 국가 별로 제공되는 서비스/법령이 상이(라이선스 별 상이)(MS의 제품 카테고리 - Productivity, Insight, Machine learning, Security 등, 이 중 우리는 Productivity에 집중)
-여러 브라우저를 통해서 user별로 로그인하여 M365 기능들을 사용해보고 어떻게 동작하는지, Teams에서 어떻게 보여지는지 체크
-스터디 : https://docs.microsoft.com/ko-kr/learn/m365/ 
-매뉴얼 : https://docs.microsoft.com/ko-kr/microsoft-365/?view=o365-worldwide
-주로 사용하게 될 사이트 목록
cdx.transform.microsoft.com
portal.office.com
portal.azure.com
admin.microsoft.com
aad.portal.azure.com
my.visualstudio.com
-브라우저 여러가지 설치할 것 : chrome, firefox, opera, microsoft edge 완료
-쿠키 : 세션 쿠키(브라우저에만 저장), 영구쿠키(disk에 저장)
-AAD를 통해 개별 서비스(portal, admin, teams)가 다 연결되어 매번 로그인없이도 바로 사용 가능 : Single sign on

(https://www.vmware.com/kr/topics/glossary/content/virtual-desktop-infrastructure-vdi.html)
-Windows 365 : VDI
-VDI(Virtual Desktop Infrastructure) : 가상 데스크톱 인프라, 가상 머신을 이용하여 가상 데스크톱을 제공하고 관리하는 것, 중앙 집중식 서버에서 데스크톱 환경을 호스트하며 요청 시 이를 최종 사용자에게 배포, VDI에서는 하이퍼바이저가 서버를 가상 머신으로 세분화하고 가상 머신은 가상 데스크톱을 호스팅하며 사용자는 각자의 기기를 통해 가상 데스크톱에 원격으로 액세스, 사용자는 장소와 기기에 구애받지 않고 가상 데스크톱에 액세스가 가능하며 모든 처리는 호스트 서버에서 이루어짐
-데스크톱 가상화 : 데스크톱 환경과 여기에 액세스하는 데 사용되는 하드웨어를 분리하는 기술을 통칭하는 용어, VDI는 데스크톱 가상화의 한 유형
-가상머신(VM, Virtual Machine) : VDI의 기반이 되는 기술(VDI 환경에서 가상 데스크톱을 실행하는 기술), 하이퍼바이저를 사용하여 하나의 물리적 서버를 여러 개의 가상 서버로 분할하여 생성된 소프트웨어 머신
-Hypervisor : 가상 머신 모니터, 가상머신을 생성하고 실행하는 프로세스
