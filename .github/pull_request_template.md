  ## 과제 체크포인트

  ### 기본과제

  - [x] shallowEquals 구현 완료
  - [x] deepEquals 구현 완료
  - [x] memo 구현 완료
  - [x] deepMemo 구현 완료
  - [x] useRef 구현 완료
  - [x] useMemo 구현 완료
  - [x] useDeepMemo 구현 완료
  - [x] useCallback 구현 완료

  ### 심화 과제

  - [x] 기본과제에서 작성한 hook을 이용하여 렌더링 최적화를 진행하였다.
  - [x] Context 코드를 개선하여 렌더링을 최소화하였다.

  ## 과제 셀프회고

  <!-- 과제에 대한 회고를 작성해주세요 -->
  이번 과제를 하면서 `memo`, `useCallback`, `useMemo`가 뭔지는 이제야 조금은 알것같습니다..
  테스트를 통과하기 위해 열심히 문서랑 검색도 해보고, 코드를 수정하면서 '아, 이게 최적화를 위한 거구나' 정도는 깨달았지만, 정확히 어떻게 동작하는지 완벽하게 이해했다고는 못하겠습니다.
  그냥 '아, 얘는 이런 상황에서 써야 한다!'는 정도로만 감정도만 잡은 상태인것같습니다.
  예를 들어, `memo`를 통해 컴포넌트 리렌더링을 줄이는 건 이해는 했지만, 
  `shallowEquals`와 `deepEquals`를 언제 써야 하는지? 상황에 따라 얕은 비교와 깊은 비교를 어떻게 조합해야 예시를 많이 봐야할것같은 생각이 들었습니다.
  솔직히 이번 과제는 느낌만 아는 상태로 진행했어요. 물론 다른 과제들도 마찬가지지만 테스트는 통과했지만, 
  그 과정에서 참으로 부족한 점이 많이 느껴지는 과제였습니다.

  ### 기술적 성장

  #### useRef와 useState
  - 이번 과제를 통해 `useRef`와 `useState`의 가장 큰 차이점을 알게되었습니다. `useState`는 상태를 업데이트할 때마다 컴포넌트가 리렌더링되지만, `useRef`는 값 변경만 수행하고 리렌더링을 하지 않죠. 그래서 리렌더링이 필요 없는 부분에서는 `useRef`를 적극적으로 활용해서 불필요한 렌더링을 줄일 수 있었어요.

  #### useMemo와 useCallback
  - `useMemo`와 `useCallback`은 이번 과제에서 사용하면서 비슷하게 느껴졌지만, 차이점을 심화과제에서 구현하면서 어느정도 느낌을 알게되었습니다..
  - **useMemo**: 연산량이 많은 값을 캐싱해서, 값이 필요할 때마다 다시 계산하지 않도록 돕는 역할을 한다는 걸 배웠어요. 이번 과제에서는 `generateItems`처럼 초기값이 큰 데이터를 캐싱하는데 활용했습니다.
  - **useCallback**: 컴포넌트가 리렌더링될 때 함수 참조를 재생성하지 않도록 도와준다는 걸 느꼈습니다. `toggleTheme` 같은 이벤트 핸들러 함수에 활용해서 불필요한 함수 재생성 방지하는데 활용했습니다.


  ### 과제 피드백
  - 지금은 '이런 상황에서 이런 걸 쓰면 된다' 는 느낌만 받았습니다. 하지만 왜 이런 동작을 하는지, 그리고 어떤 경우에 더 효과적인지에 대한 명확한 이해는 부족한 것 같아요.
  - `AppContext`, `ThemeContext`, `NotificationContext`를 분리해서 상태를 관리하는 건 해냈지만, `Context`가 리렌더링에 미치는 영향에 대해 더 깊이 이해해야 할 것 같아요.

  ### 다음 목표

  - 이번 과제에서 다룬 `memo`, `useCallback`, `useMemo`를 정확히 이해하기 위해 관련 문서를 찾아봐야할것같습니다.
  - 얕은 비교와 깊은 비교의 성능 차이의 실험 그리고 어떤 상황에서 각각을 써야 하는지 감을 잡고 싶습니다.
  - React DevTools로 리렌더링이 발생하는 이유를 추적해서 어떤 상태 변경이 어떤 컴포넌트에 영향을 주는지 분석하는 연습
