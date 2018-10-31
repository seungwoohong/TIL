# Lazy looading

> Angular 는 비동기 라우팅이 가능하다. 기능들을 모듈로 분리하고 나중에 필요한 모듈을 사용자가 > 필요할 때 불러오는 것이다. 이러한 기술을 Lazy loading 이라고 하는데 이렇게 되면 SPA의  > 단점인 긴 초기로딩 시간을 줄 일 수 있다.

```javascript
const appRoutes: Routes = [
  { path: '', loadChildren: './pages/pages.module#PagesModule' }
];

@NgModule({
  imports: [
    RouterModule.forRoot(
      appRoutes,
      { enableTracing: true } // <-- debugging purposes only
    )
  ],
  exports: [RouterModule]
})
export class AppRoutingModule {}
```
> loadChildren key를 사용 하여 모듈을 불러오는데 초기에 불러오는 것이 아니라 해당 패스로 들어오게 되면 로딩된다.

```javascript
import { NgModule } from '@angular/core';
import { Routes, RouterModule } from '@angular/router';
import { NoContentComponent } from './no-content/no-content.component';
import { LoginComponent } from './login/login.component';

const routes: Routes = [
  { path: '', component: LoginComponent },
  { path: '**', component: NoContentComponent }
];

@NgModule({
  imports: [RouterModule.forChild(routes)],
  exports: [RouterModule]
})
export class PagesRoutingModule {}
```

**forRoot** 와 **forChild**의 차이는 다음과 같다. forRoot는 appRoutes의 정보를 함쳐서 어플리케이션 단위의 모듈로 만들어 주는 역할을 한다. 따라서 루트 모듈에서만 사용 되며 시작 포인트를 갖게 된다. forCHild는 자식 모듈들의 라우터들을 취함하고 해당 모듈의 포인트를 갖게 된다.
