---
layout: post
title: "JavaScript 비동기 처리 완벽 정리: Callback → Promise → async/await"
description: "콜백 지옥에서 async/await까지, JavaScript 비동기 처리의 진화 과정을 코드 예제와 함께 이해합니다."
date: 2025-01-22
tags: [JavaScript, 비동기]
---

JavaScript는 싱글 스레드 언어임에도 비동기 처리를 통해 효율적으로 작업합니다. 비동기 패턴이 어떻게 발전해왔는지 살펴봅시다.

## 1. Callback — 시작점

가장 기본적인 비동기 패턴:

```javascript
function fetchData(url, callback) {
  setTimeout(() => {
    const data = { id: 1, name: "Alice" };
    callback(null, data);
  }, 1000);
}

fetchData("/api/user", (err, data) => {
  if (err) return console.error(err);
  console.log(data); // { id: 1, name: "Alice" }
});
```

### 콜백 지옥 (Callback Hell)

중첩이 깊어지면 코드 가독성이 급격히 떨어집니다:

```javascript
getUser(userId, (err, user) => {
  getPosts(user.id, (err, posts) => {
    getComments(posts[0].id, (err, comments) => {
      // 점점 깊어지는 들여쓰기...
    });
  });
});
```

## 2. Promise — 구원자

ES6에서 도입된 Promise로 체이닝이 가능해졌습니다:

```javascript
function fetchUser(id) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (id > 0) resolve({ id, name: "Alice" });
      else reject(new Error("Invalid ID"));
    }, 1000);
  });
}

fetchUser(1)
  .then(user => fetchPosts(user.id))
  .then(posts => fetchComments(posts[0].id))
  .then(comments => console.log(comments))
  .catch(err => console.error(err));
```

### Promise.all — 병렬 처리

```javascript
const [users, posts] = await Promise.all([
  fetchUsers(),
  fetchPosts()
]);
```

## 3. async/await — 현재의 표준

ES2017에서 도입. 비동기 코드를 동기처럼 읽을 수 있습니다:

```javascript
async function loadDashboard(userId) {
  try {
    const user = await fetchUser(userId);
    const posts = await fetchPosts(user.id);
    const comments = await fetchComments(posts[0].id);
    return { user, posts, comments };
  } catch (err) {
    console.error("로드 실패:", err);
    throw err;
  }
}
```

> **핵심**: `async` 함수는 항상 Promise를 반환합니다. `await`는 `async` 함수 내부에서만 사용 가능합니다.

## 어떤 패턴을 써야 할까?

| 상황 | 추천 |
|------|------|
| 레거시 코드 유지보수 | Callback (어쩔 수 없는 경우) |
| 이벤트 스트림 처리 | Promise / Observable |
| 일반적인 비동기 처리 | **async/await** |
| 여러 비동기 병렬 처리 | **Promise.all** |

## 마치며

현대 JavaScript 개발에서는 `async/await`를 기본으로 사용하되, `Promise.all`로 병렬 처리를 최적화하는 패턴을 익혀두면 좋습니다.
