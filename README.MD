# 스프링 입문
출처: [김영한님 인프런 강의](https://www.inflearn.com/course/%EC%8A%A4%ED%94%84%EB%A7%81-%EC%9E%85%EB%AC%B8-%EC%8A%A4%ED%94%84%EB%A7%81%EB%B6%80%ED%8A%B8/dashboard)

## 스프링을 이용하여 회원 관리 서비스 생성

### Domain
- [Member.java](src/main/java/hello/hellospring/domain/Member.java)

### Controller
- [MemberController.java](src/main/java/hello/hellospring/controller/MemberController.java)
- [MemberForm.java](src/main/java/hello/hellospring/controller/MemberForm.java) (화면에서 입력받는 내용 매핑)

### Service
- [MemberService.java](src/main/java/hello/hellospring/service/MemberService.java)
    - 회원 가입
    - Id로 회원 조회하기
    - 이름으로 회원 조회하기
    - 모든 회원 목록 조회하기
    
### Repository
- [MemberRepository.java](src/main/java/hello/hellospring/repository/MemberRepository.java) interface
1. 순수 Jdbc
    - [JdbcMemberRepository.java](src/main/java/hello/hellospring/repository/JdbcMemberRepository.java)
    
2. 스프링 JdbcTemplate
    - [JdbcTemplateMemberRepository.java](src/main/java/hello/hellospring/repository/JdbcTemplateMemberRepository.java)
    
3. Jpa
    - [JpaMemberRepository.java](src/main/java/hello/hellospring/repository/JpaMemberRepository.java)
    
4. 스프링 데이터 Jpa
    - [SpringDataJpaMemberRepository.java](src/main/java/hello/hellospring/repository/SpringDataJpaMemberRepository.java)
    
- [SpringConfig.java](src/main/java/hello/hellospring/SpringConfig.java) 에서 설정 변경 가능
- [MemberServiceIntegrationTest.java](src/test/java/hello/hellospring/service/MemberServiceIntegrationTest.java) 에서 스프링 통합 테스트 가능