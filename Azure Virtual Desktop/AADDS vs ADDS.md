![[AADDS vs ADDS image.png]]

> Azure Portal을 사용하여 도메인 컨트롤러 VM을 종료하지 않는 것이 좋습니다. 대신 게스트 운영 체제를 종료하고 다시 시작하십시오. Azure Portal을 통해 종료하면 VM 할당이 취소되어 도메인 컨트롤러 VM을 다시 시작할 때 다음과 같은 결과가 발생합니다.

1.  Sync 방향
    1.  IaaS : AD -> AAD
    2.  AADDS : AAD -> AADDS 
2.  관리(보안, 패치, 백업 등)
	1.  IaaS : Cloocus
		1.  Basic : [Deploy AD DS in an Azure virtual network | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/reference-architectures/identity/adds-extend-domain)  
		2. Security : [Best Practices for Securing Active Directory | Microsoft Learn](https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/best-practices-for-securing-active-directory)
		3. Perf : [Performance Tuning Active Directory Servers | Microsoft Learn](https://learn.microsoft.com/en-us/windows-server/administration/performance-tuning/role/active-directory-server/)
	2. AADDS : MS
3. Domain Admin / Enterprise Admin
    1.  IaaS : 사용 가능
    2.  AADDS : 사용 불가
        1.  Enterprise Admins
            1.  포리스트 루트 도메인의 관리자
                1.  포리스트 트러스트 설정, 아웃바운드 트러스트 구축 등  
        2.  Domain Admins
            1.  해당 도메인 내의 관리자






  