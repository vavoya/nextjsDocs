- **목적**: `draftMode` 함수는 서버 컴포넌트 내에서 Draft Mode(초안 모드)의 활성화 여부를 감지하는 데 사용됩니다.

- **사용 예시**: 
  ```javascript
  import { draftMode } from 'next/headers'

  export default function Page() {
    const { isEnabled } = draftMode()
    return (
      <main>
        <h1>My Blog Post</h1>
        <p>Draft Mode is currently {isEnabled ? 'Enabled' : 'Disabled'}</p>
      </main>
    )
  }
  ```
  이 예시에서, `draftMode`는 `next/headers`에서 가져온 후, `draftMode()` 함수로부터 반환된 `isEnabled` 속성을 사용하여 Draft Mode의 활성화 상태를 확인합니다

이 함수는 서버 렌더링 컴포넌트에서 초안 및 게시 상태를 전환하는 데 유용하며, 개발자가 모드에 따라 다른 콘텐츠나 기능을 처리할 수 있게 해줍니다.