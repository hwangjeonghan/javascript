- Thymeleaf는 뭐야?
    
    Thymeleaf는 Spring Framework와의 모듈, 여러분이 좋아하는 도구와의 통합, 그리고 자신의 기능을 플러그인 할 수 있는 능력 등을 통해 현대의 HTML5 JVM 웹 개발에 이상적입니다. 또한, Thymeleaf로 작성된 HTML 템플릿은 브라우저에서 그대로 표시되므로, 실제로 애플리케이션에서 실행되는 템플릿이 유용한 디자인 아티팩트로 작동할 수 있습니다.
    
    Thymeleaf는 Eclipse, IntelliJ IDEA, Spring, Play 등과 같은 도구와 통합되어, 웹 개발 프레임워크를 사용하여 Thymeleaf를 작성할 수 있습니다. 또한, Thymeleaf는 순수한 HTML을 최대한 유지하려는 특징이 있습니다. 타임리프로 작성한 파일은 HTML을 유지하기 때문에 웹 브라우저에서 파일을 직접 열어도 내용을 확인할 수 있습니다. 이러한 특징을 네츄럴 템플릿 (Natural Template)이라고 합니다.
    
    Thymeleaf는 서버상에서 동작하지 않아도 HTML 파일의 내용을 바로 확인이 가능하다는 특징을 가지고 있습니다. 이는 독립적으로 UI 템플릿 작업을 수행하는 데 매우 유용하며, 실행 중인 서버가 필요 없습니다.
    
- Thymeleaf는 왜 사용하는거야? —> 화면 확인에 용이함
    
    Thymeleaf를 사용하는 이유는 여러 가지가 있습니다:
    
    1. **네츄럴 템플릿**: Thymeleaf는 순수한 HTML을 최대한 유지하려는 특징이 있습니다. 타임리프로 작성한 파일은 HTML을 유지하기 때문에 웹 브라우저에서 파일을 직접 열어도 내용을 확인할 수 있습니다. 이러한 특징을 네츄럴 템플릿 (Natural Template)이라고 합니다.
    2. **서버 사이드 HTML 렌더링 (SSR)**: 타임리프는 백엔드 서버에서 HTML을 동적으로 렌더링하는 용도로 사용됩니다. 페이지가 어느정도 동적이고 빠른 생산성이 필요한 화면을 만드는 경우 좋은 선택지가 될 수 있습니다.
    3. **스프링 통합 지원**: 타임리프는 스프링과 자연스럽게 통합되어 스프링의 다양한 기능을 쉽게 사용할 수 있습니다.
    4. **효율성**: Thymeleaf는 애플리케이션에서 생성된 데이터를 템플릿 파일로 파싱하고 렌더링하는 Java 라이브러리이며, 템플릿 엔진입니다. 이는 파싱된 데이터/파일을 캐싱하여 생산성을 높이는 데 도움이 됩니다.
    
    따라서, Thymeleaf는 웹 개발자들에게 많은 이점을 제공하며, 이러한 이유로 많이 사용됩니다. Thymeleaf를 사용하면 개발자는 애플리케이션 템플릿을 효과적으로 설계하고, 동적인 웹 페이지를 쉽게 생성할 수 있습니다.
    
- View Resolver
    
    "View Resolver"는 Spring MVC에서 사용되는 개념으로, Controller에서 반환된 논리적인 뷰 이름을 실제 뷰 객체, 예를 들어 JSP나 Thymeleaf 템플릿 등으로 매핑하는 역할을 합니다.
    
- View Resolver 왜 쓰는거야?
    
    Spring MVC에서 View Resolver는 컨트롤러(Controller)가 반환하는 논리적인 뷰 이름(예: ‘home’)을 실제 뷰 객체(예: ‘home.jsp’)로 변환해주는 역할을 합니다. 이를 통해 개발자는 뷰의 실제 경로나 기술에 대해 걱정할 필요 없이 비즈니스 로직에 집중할 수 있습니다. 이것이 View Resolver를 사용하는 이유입니다.