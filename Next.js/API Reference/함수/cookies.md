Next.js의 `cookies` 함수들은 HTTP 요청 및 응답에 사용되는 쿠키와 관련된 여러 기능을 제공합니다​​:

1. **`cookies().get(name)`**: 특정 이름의 쿠키를 찾아 그 이름과 값을 객체로 반환합니다. 해당 이름의 쿠키가 없으면 `undefined`를 반환하며, 같은 이름의 쿠키가 여러 개 있을 경우 첫 번째 쿠키만 반환합니다​[](https://nextjs.org/docs/app/api-reference/functions/cookies)​.
    
2. **`cookies().getAll()`**: `get`과 유사하지만, 지정된 이름의 모든 쿠키들을 리스트로 반환합니다. 이름이 지정되지 않으면 사용 가능한 모든 쿠키를 반환합니다​[](https://nextjs.org/docs/app/api-reference/functions/cookies#:~:text=,only%20return%20the%20first%20match)​.
    
3. **`cookies().has(name)`**: 지정된 이름의 쿠키가 존재하는지 여부를 불리언 값(`true` 또는 `false`)으로 반환합니다​[](https://nextjs.org/docs/app/api-reference/functions/cookies#:~:text=,returns%20all%20the%20available%20cookies)​.
    
4. **`cookies().set(name, value, options)`**: 쿠키 이름, 값, 옵션을 사용하여 새로운 쿠키를 설정합니다. 이 메소드는 요청의 응답에 쿠키를 설정하는 데 사용됩니다​[](https://nextjs.org/docs/app/api-reference/functions/cookies#:~:text=,false)​.
    
5. **쿠키 삭제**: 쿠키는 `Server Action` 또는 `Route Handler`에서만 삭제할 수 있습니다​[](https://nextjs.org/docs/app/api-reference/functions/cookies#:~:text=,sets%20the%20outgoing%20request%20cookie)​.
    
    - **`cookies().delete(name)`**: 지정된 이름의 쿠키를 명시적으로 삭제합니다​[](https://nextjs.org/docs/app/api-reference/functions/cookies#:~:text=,22%E2%80%A0Route%20Handler%E3%80%91)​.
    - **`cookies().set(name, '')`**: 동일한 이름으로 새 쿠키를 빈 값으로 설정하여 삭제하는 방법입니다​[](https://nextjs.org/docs/app/api-reference/functions/cookies#:~:text=,cookie%20with%20a%20given%20name)​.
    - **`cookies().set(name, value, { maxAge: 0 })`**: `maxAge`를 0으로 설정하여 쿠키를 즉시 만료시킵니다​[](https://nextjs.org/docs/app/api-reference/functions/cookies#:~:text=,name%20and%20an%20empty%20value)​.
    - **`cookies().set(name, value, { expires: timestamp })`**: `expires`를 과거의 어떤 값으로 설정하여 쿠키를 즉시 만료시킵니다​[](https://nextjs.org/docs/app/api-reference/functions/cookies#:~:text=,will%20immediately%20expire%20a%20cookie)​.